<template>
  <v-text-field
    :value="formatted"
    type="text"
    placeholder="Your phone number"
    class="custom-input"
    @input="acceptNumber">
  </v-text-field>
</template>

<script>
import { helpers } from 'vuelidate/lib/validators';

const isValidPhone = helpers.regex("isValidPhone",/^(\d{1,2}\s)?\(?\d{3}\)?[\s.-]\d{3}[\s.-]\d{4}$/);

export default {
    props: {
        value: { type: String, required: true }
    },
    data() {
        return {
            phone: this.value
        }
    },
    computed: {
        cleaned() {
            return this.phone.replace(/\D/g,'');
        },
        formatted() {
            const x = this.phone.replace(/\D/g,'').match(/(\d{0,3})(\d{0,3})(\d{0,4})/);
            return !x[2] ? x[1] : '(' + x[1] + ') ' + x[2] + (x[3] ? '-' + x[3] : '');
        }
    },
    methods: {
        acceptNumber(input) {
            this.phone = input;

            const val = isValidPhone(input)? this.cleaned : '';
            this.$emit('input', val);
        }
    }
}
</script>