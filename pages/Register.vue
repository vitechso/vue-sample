<template>
  <div>
    <section class="Login-banner">
      <v-container>
        <v-row>
          <v-col lg="12" class="Login-Col">
            <div class="Login-Container wow fadeIn">
              <router-link to="/" class="BrandLogo">
                <img alt="Vue logo" src="@/assets/logo/logo.svg" />
              </router-link>

              <img src="@/assets/img/shampooCloud.png" class="Cloud-bg" />

              <div class="Login-Details SignUp-Details">
                <div class="LoginTitle">
                  <h2>Sign up</h2>
                  <p>
                    You are moments away from a barking fantastic scheduling system.
                  </p>
                </div>

                <div class="form-group">
                  <v-text-field
                    v-model="user.company_name"
                    type="text"
                    placeholder="Company Name"
                    class="custom-input"
                  ></v-text-field>
                  <div v-if="submitted && !$v.user.company_name.required" class="invalid-feedback">Company Name is required</div>
                </div>

                <div class="form-group">
                  <v-text-field
                    v-model="user.first_name"
                    type="text"
                    placeholder="First Name"
                    class="custom-input"
                  ></v-text-field>
                  <div v-if="submitted && !$v.user.first_name.required" class="invalid-feedback">First Name is required</div>
                </div>

                <div class="form-group">
                  <v-text-field
                    v-model="user.last_name"
                    type="text"
                    placeholder="Last Name"
                    class="custom-input"
                  ></v-text-field>
                  <div v-if="submitted && !$v.user.last_name.required" class="invalid-feedback">Last Name is required</div>
                </div>

                <div class="form-group">
                  <v-text-field
                    v-model="user.phone_number"
                    type="number"
                    placeholder="Contact Number"
                    class="custom-input"
                  ></v-text-field>
                  <div v-if="submitted && !$v.user.phone_number.required" class="invalid-feedback">Contact Number is required</div>
                </div>

                <div class="form-group">
                  <v-text-field
                    v-model="user.email"
                    type="email"
                    placeholder="Email Address"
                    class="custom-input"
                  ></v-text-field>
                  <div v-if="submitted && !$v.user.email.required" class="invalid-feedback">Email is required</div>
                  <div v-if="submitted && !$v.user.email.email" class="invalid-feedback">Invalid email</div>
                </div>

                <div class="form-group">
                  <v-text-field
                    v-model="user.password"
                    type="password"
                    placeholder="Password"
                    class="custom-input"
                  ></v-text-field>
                  <div v-if="submitted && !$v.user.password.minLength" class="invalid-feedback">Password should atleast be 8 characters long</div>
                  <div v-if="submitted && !$v.user.password.required" class="invalid-feedback">Password is required</div>
                </div>

                <div class="form-group">
                  <v-text-field
                    v-model="user.confirm_password"
                    type="password"
                    placeholder="Confirm Password"
                    class="custom-input"
                  ></v-text-field>
                  <div v-if="submitted && !$v.user.confirm_password.required" class="invalid-feedback">Confirm Password is a required field</div>
                  <div v-if="submitted && !$v.user.confirm_password.sameAsPassword" class="invalid-feedback">Confirm Password should match password</div>
                </div>

                <div class="form-group">
                  <v-text-field
                    v-model="user.promo_code"
                    type="text"
                    placeholder="Promo Code (optional)"
                    class="custom-input"
                  ></v-text-field>
                </div>

                <div class="form-group TermsCheck">
                  <v-checkbox
                    v-model="user.accepted_tos"
                    label="I have read & agreed to the"
                    color="primary"
                    hide-details
                  ></v-checkbox>

          <router-link target="_blank" to="/terms"> Terms of Service </router-link>


                </div>

                <div v-if="submitted && !$v.user.accepted_tos.sameAsTrue" class="invalid-feedback topupper">Please accept terms of services</div>

                <div class="form-group Login-Btn">
                 
                    <v-btn
                      class="
                        ThemeBtn
                        animate__animated animate__bounceIn animate__delay-2s
                      "
                      @click="signUp"
                      >Create My Account</v-btn
                    >
                
                </div>



                <div class="form-group">
                  <a target="_blank" href="https://groomer.io/login" class="Go-account">Or, already have an account?</a>
                </div>

                <div class="form-group">


                  <a target="_blank" href="https://groomer.io/login">
                    <v-btn class=" ThemeBtn GrayBtn animate__animated animate__bounceIn animate__delay-2s">Log in</v-btn>
                  </a>
                </div>
              </div>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </section>
  </div>
</template>

<script>
import { required,email,minLength,sameAs } from 'vuelidate/lib/validators';

export default {
  layout: 'login',
  data(){
    return{
      user: {
        company_name: '',
        last_name: '',
        first_name: '',
        email: '',
        phone_number: '',
        password: '',
        confirm_password: '',
        accepted_tos:false,
        promo_code: null,
      },
      submitted: false
    }
  },
  validations:{
    user:{
    phone_number:{
      required
    },
    company_name:{
      required
    },
    last_name:{
      required
    },
    first_name:{
      required
    },
    email:{
      required,
      email
    },
    password:{
      required,
      minLength:minLength(8)
    },
    confirm_password:{
      required,
      sameAsPassword:sameAs('password')
    },
    accepted_tos: {
      sameAsTrue: sameAs(() => true)
    },
    }
  },
  methods:{
    signUp(){
      this.$data.submitted = true;
      this.$v.$touch();
      if (this.$v.$invalid) {
        return false;
      } else {
        const user = {...this.$v.user.$model};
        delete user.confirm_password;
        this.$axios.post('/api/public/v1/register',user).then((res)=>{
          this.$toast.success('Registered successfully..!!');
          window.location.href = res.data.link;
        }).catch((err)=>{
          if(err?.response?.data?.error_message){
            this.$toast.error(err.response.data.error_message)
          }else{
            this.$toast.success('Something went wrong...please try after sometime');
          }
        })
      }
    },
  }
}
</script>
