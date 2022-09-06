<template>
  <div>
    <section class="HomeBanner light-pink">
      <v-container>
        <v-row class="col-reverse-sm">
          <v-col cols="12" sm="6" md="6" lg="6" class="">
            <div class="Banner-Details">
              <h1>
                Make your grooming business
                <span>easier <img src="@/assets/img/text-circle.svg" /></span>
                and more profitable.
              </h1>
              <h5>Groomer.io, The App Made Just For Groomers</h5>

              <router-link to="/register">
                <v-btn class="ThemeBtn" data-wow-delay="0.5s"
                  >Try for free</v-btn
                >
              </router-link>

              <div class="AppStore-Btns" data-wow-delay="0.5s">
                <a
                  target="_blank"
                  href="https://apps.apple.com/us/app/groomer-io/id1001294431">
                    <img src="@/assets/img/AppStore.svg"/>
                </a>
                <a
                  target="_blank"
                  href="https://play.google.com/store/apps/details?id=com.groomer.groomerio"
                  ><img src="@/assets/img/PlayStore.svg"
                /></a>
              </div>
            </div>
          </v-col>

          <v-col cols="12" sm="6" md="6" lg="6" class="">
            <div class="Banner-Circle-Info">
              <div class="Inner-Circle-Info">
                <div class="Img-Info wow fadeIn" data-wow-delay="1s">
                  <img src="@/assets/img/banner-img.png" />
                </div>

                <div
                  class="Comment-Info wow lightSpeedIn"
                  data-wow-delay="1.5s"
                >
                  <div class="Img-Box">
                    <img src="@/assets/img/cmnt-img01.png" />
                  </div>
                  <div class="Comment-details">
                    <p>Diego is clean, shiny and ready to pick up!</p>
                  </div>
                </div>

                <div
                  class="Comment-Info comment-2 wow lightSpeedIn"
                  data-wow-delay="1.5s"
                >
                  <div class="Img-Box">
                    <img src="@/assets/img/cmnt-img02.png" />
                  </div>
                  <div class="Comment-details">
                    <p>Great, will pick him up asap!</p>
                  </div>
                </div>

                <div class="comment-3 wow lightSpeedIn" data-wow-delay="1.5s">
                  <div class="Date-Box">
                    <h6>Oct</h6>
                    <h5>14</h5>
                  </div>

                  <div class="Box-details">
                    <span>2:30 PM</span>
                    <p>Diego - <span>Lux Cut</span></p>
                  </div>
                </div>

                <div class="wow lightSpeedIn" data-wow-delay="1.5s">
                  <div class="Tip-Info">
                    <div class="Titles">
                      <h4>Add a tip?</h4>
                      <p>
                        Happy with your pets fresh look? Say thanks to the
                        Groomer.
                      </p>
                    </div>

                    <div class="Tip-grid">
                      <div class="Grid-box">
                        <h3>15%</h3>
                        <p>$30.15</p>
                      </div>

                      <div class="Grid-box">
                        <h3>20%</h3>
                        <p>$45.70</p>
                      </div>

                      <div class="Grid-box active">
                        <h4>Average tip</h4>
                        <h3>22.2%</h3>
                        <p>$60.12</p>
                      </div>

                      <div class="Grid-box">
                        <h3>25%</h3>
                        <p>$60.12</p>
                      </div>
                    </div>

                    <div class="Tip-Btns">
                      <a href="#">I’ll tip in person</a>
                      <a href="#">Custom amount</a>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </v-col>
        </v-row>
      </v-container>

      <img src="@/assets/img/sky-bg.png" class="sky-bg" />
    </section>

    <!-- //Section Second -->

    <section class="custom-space pb-0 overflow-hidden">
      <v-container fluid>
        <v-row>
          <v-col lg="12">
            <div class="Section-Title center">
              <h2 class="main-head wow fadeInUp">
                Trusted by over 2000 groomers
              </h2>
            </div>
          </v-col>
        </v-row>

        <v-row>
          <v-col lg="12">
            <div class="swiper-container">
              <!-- <v-carousel hide-delimiters :interval="6000" :show-arrows="false" cycle height="150"> 
                <template v-for="(item, index) in slider"> 
                  <v-carousel-item v-if="(index + 1) % columns === 2 || columns === 2" :key="index"> 
                    <v-row class="flex-nowrap" align="center"> 
                      <template v-for="(n,i) in columns">
                        <template v-if="(+index + i) < slider.length"> 
                          <v-col :key="i"> 
                            <v-sheet v-if="(+index + i) < slider.length">
                              <v-row
                                    align="center"
                                    justify="center"
                              >
                             
                                <div class="display-3 ClientLogo"><img class="ImgFlud" :src="require(`../assets/img/logos/${slider[+i+index]}`)" alt=""></div>
                              </v-row>
                            </v-sheet>
                          </v-col> 
                        </template> 
                      </template> 
                    </v-row> 
                  </v-carousel-item> 
                </template> 
              </v-carousel> -->

              <!-- <div class="slider">
                <div class="slide-track">
                  <div class="slide">
                    <img
                      src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/557257/1.png"
                      height="100"
                      width="250"
                      alt=""
                    />
                  </div>
                  <div class="slide">
                    <img
                      src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/557257/2.png"
                      height="100"
                      width="250"
                      alt=""
                    />
                  </div>
                  <div class="slide">
                    <img
                      src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/557257/3.png"
                      height="100"
                      width="250"
                      alt=""
                    />
                  </div>
                  <div class="slide">
                    <img
                      src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/557257/4.png"
                      height="100"
                      width="250"
                      alt=""
                    />
                  </div>
                  <div class="slide">
                    <img
                      src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/557257/5.png"
                      height="100"
                      width="250"
                      alt=""
                    />
                  </div>
                  <div class="slide">
                    <img
                      src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/557257/6.png"
                      height="100"
                      width="250"
                      alt=""
                    />
                  </div>
                  <div class="slide">
                    <img
                      src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/557257/7.png"
                      height="100"
                      width="250"
                      alt=""
                    />
                  </div>
                  <div class="slide">
                    <img
                      src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/557257/1.png"
                      height="100"
                      width="250"
                      alt=""
                    />
                  </div>
                  <div class="slide">
                    <img
                      src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/557257/2.png"
                      height="100"
                      width="250"
                      alt=""
                    />
                  </div>
                  <div class="slide">
                    <img
                      src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/557257/3.png"
                      height="100"
                      width="250"
                      alt=""
                    />
                  </div>
                  <div class="slide">
                    <img
                      src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/557257/4.png"
                      height="100"
                      width="250"
                      alt=""
                    />
                  </div>
                  <div class="slide">
                    <img
                      src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/557257/5.png"
                      height="100"
                      width="250"
                      alt=""
                    />
                  </div>
                  <div class="slide">
                    <img
                      src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/557257/6.png"
                      height="100"
                      width="250"
                      alt=""
                    />
                  </div>
                  <div class="slide">
                    <img
                      src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/557257/7.png"
                      height="100"
                      width="250"
                      alt=""
                    />
                  </div>
                </div>
              </div> -->
              <VueSlickCarousel v-bind="Settings" class="Client-Logos">
                <div class="CL-Logo-Info">
                  <img
                    src="../assets/img/logos/BlueDog.png"
                    alt="Natural"
                    class="Img-left"
                  />
                </div>
                <div class="CL-Logo-Info">
                  <img
                    src="../assets/img/logos/BowWow.png"
                    alt="Natural"
                    class="Img-left"
                  />
                </div>
                <div class="CL-Logo-Info">
                  <img
                    src="../assets/img/logos/Choye.png"
                    alt="Natural"
                    class="Img-left"
                  />
                </div>
                <div class="CL-Logo-Info">
                  <img
                    src="../assets/img/logos/ClippinTails.png"
                    alt="Natural"
                    class="Img-left"
                  />
                </div>
                <div class="CL-Logo-Info">
                  <img
                    src="../assets/img/logos/DogPerfect.png"
                    alt="Natural"
                    class="Img-left"
                  />
                </div>
                <div class="CL-Logo-Info">
                  <img
                    src="../assets/img/logos/HairySofa.png"
                    alt="Natural"
                    class="Img-left"
                  />
                </div>
                <div class="CL-Logo-Info">
                  <img
                    src="../assets/img/logos/HydroDog.png"
                    alt="Natural"
                    class="Img-left"
                  />
                </div>
                <div class="CL-Logo-Info">
                  <img
                    src="../assets/img/logos/KristiFancyK9.png"
                    alt="Natural"
                    class="Img-left"
                  />
                </div>
                <div class="CL-Logo-Info">
                  <img
                    src="../assets/img/logos/PerfectPaw.png"
                    alt="Natural"
                    class="Img-left"
                  />
                </div>
                <div class="CL-Logo-Info">
                  <img
                    src="../assets/img/logos/PureJoy.png"
                    alt="Natural"
                    class="Img-left"
                  />
                </div>
                <div class="CL-Logo-Info">
                  <img
                    src="../assets/img/logos/SDGA.png"
                    alt="Natural"
                    class="Img-left"
                  />
                </div>
                <div class="CL-Logo-Info">
                  <img
                    src="../assets/img/logos/Shakers.png"
                    alt="Natural"
                    class="Img-left"
                  />
                </div>
                <div class="CL-Logo-Info">
                  <img
                      src="../assets/img/logos/VanderpumpDogs.png"
                      alt="Natural"
                      class="Img-left"
                    />
                </div>
                <div class="CL-Logo-Info">
                  <img
                      src="../assets/img/logos/VanityFur.png"
                      alt="Natural"
                      class="Img-left"
                    />
                </div>
                <div class="CL-Logo-Info">
                  <img
                      src="../assets/img/logos/VIP.png"
                      alt="Natural"
                      class="Img-left"
                    />
                </div>
                <div class="CL-Logo-Info">
                  <img
                      src="../assets/img/logos/WagNWash.png"
                      alt="Natural"
                      class="Img-left"
                    />
                </div>
                <div class="CL-Logo-Info">
                  <img
                      src="../assets/img/logos/YourGroomers.png"
                      alt="Natural"
                      class="Img-left"
                    />
                </div>
              </VueSlickCarousel>

              <!-- <marquee direction="left">
                <span>
                  <img src="../assets/img/logos/BlueDog.png" alt="Natural" class="Img-left" />
                <img src="../assets/img/logos/BowWow.png" alt="Natural" class="Img-left" />
                <img src="../assets/img/logos/Choye.png" alt="Natural" class="Img-left" />
                <img src="../assets/img/logos/ClippinTails.png" alt="Natural" class="Img-left" />
                <img src="../assets/img/logos/DogPerfect.png" alt="Natural" class="Img-left" />
                <img src="../assets/img/logos/HairySofa.png" alt="Natural" class="Img-left" />
                <img src="../assets/img/logos/HydroDog.png" alt="Natural" class="Img-left" />
                <img src="../assets/img/logos/KristiFancyK9.png" alt="Natural" class="Img-left" />
                <img src="../assets/img/logos/PerfectPaw.png" alt="Natural" class="Img-left" />
                </span>
                
                <span>
                  <img src="../assets/img/logos/PureJoy.png" alt="Natural" class="Img-left" />
                <img src="../assets/img/logos/SDGA.png" alt="Natural" class="Img-left" />
                <img src="../assets/img/logos/Shakers.png" alt="Natural" class="Img-left" />
                <img src="../assets/img/logos/VanderpumpDogs.png" alt="Natural" class="Img-left" />
                <img src="../assets/img/logos/VanityFur.png" alt="Natural" class="Img-left" />
                <img src="../assets/img/logos/VIP.png" alt="Natural" class="Img-left" />
                <img src="../assets/img/logos/WagNWash.png" alt="Natural" class="Img-left" />
                <img src="../assets/img/logos/YourGroomers.png" alt="Natural" class="Img-left" />
                </span>
              </marquee> -->
            </div>
          </v-col>
        </v-row>
      </v-container>
    </section>

    <section class="custom-space">
      <v-container>
        <v-row class="mb-0 mb-md-5">
          <v-col lg="12">
            <div class="Section-Title center">
              <h2 class="sub-head wow fadeInUp" data-wow-delay="0.2s">
                Groomer.io fits
                <span
                  >your way <img src="@/assets/img/text-circle-gray.svg"
                /></span>
                of doing things
              </h2>
            </div>
          </v-col>
        </v-row>

        <v-row class="" justify="center">
          <v-col lg="4" md="4" cols="12">
            <div class="Grooming-Box">
              <div class="icon wow bounce" data-wow-delay="1s">
                <img src="@/assets/img/MobileGrooming.svg" />
              </div>

              <h2>Mobile Grooming</h2>
              <ul>
                <li>Smart Mapping & Scheduling</li>
                <li>Automated Enroute Call & SMS</li>
                <li>ETA and Departure Reminders</li>
              </ul>

              <router-link to="/mobile">
                <v-btn class="Learmore-btn">Learn more</v-btn>
              </router-link>
            </div>
          </v-col>

          <v-col lg="4" md="4" cols="12">
            <div class="Grooming-Box">
              <div class="icon wow bounce" data-wow-delay="1s">
                <img src="@/assets/img/GroomingSalon.svg" />
              </div>

              <h2>Grooming Salon</h2>
              <ul>
                <li>Appointment Completed Call & SMS</li>
                <li>Track Appointment Working Status</li>
                <li>Automated Comeback Reminders</li>
              </ul>

              <router-link to="/storefront">
                <v-btn class="Learmore-btn">Learn more</v-btn>
              </router-link>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </section>

    <section class="custom-space bg-gray Best-Clippers">
      <v-container>
        <v-row class="mb-0 mb-md-5">
          <v-col lg="12">
            <div class="Section-Title center">
              <h2 class="sub-head wow fadeInUp">
                The best clippers in the game about Groomer.io
              </h2>
            </div>
          </v-col>
        </v-row>

        <!-- For mobile  -->
        <div class="d-flex d-md-none BestClippers-Info">
          <v-row class="">
            <v-col lg="12">
              <div class="Testimoniasasl">
                <v-carousel hide-delimiters height="auto" cricle>
                  <v-carousel-item v-for="(item, i) in items" :key="i">
                    <div class="Clippers-Container">
                      <div class="Clippers-Info wow fadeIn">
                        <div class="Profile-Info">
                          <img :src="require(`../assets/img/${item.img}`)" />
                        </div>

                        <div class="Profile-Details">
                          <h3>{{ item.hading }}</h3>
                          <!-- eslint-disable vue/no-v-html -->
                          <p v-html="item.paragraph"></p>
                          <!--eslint-enable-->

                          <div v-if="item.InstaId" class="Feed">
                            <a :href="item.Link">
                              <div class="icon-box">
                                <img src="@/assets/img/insta.svg" />
                              </div>

                              <div class="Feed-details">
                                <h4>{{ item.InstaId }}</h4>
                                <h5>{{ item.FollowerK }}</h5>
                              </div>
                            </a>
                          </div>
                        </div>
                      </div>
                    </div>
                  </v-carousel-item>
                </v-carousel>
              </div>
            </v-col>
          </v-row>
        </div>
        <!-- For mobile end -->

        <div class="d-none d-md-flex Testimonial">
          <v-row justify="center">
            <v-col lg="9" md="10" cols="12">
              <v-carousel hide-delimiters height="auto">
                <v-carousel-item v-for="(item, i) in items_con" :key="i">
                  <div class="Clippers-Container">
                    <div
                      v-if="item.hading_one"
                      class="Clippers-Info wow fadeIn"
                      data-wow-delay=".2s"
                    >
                      <div class="Profile-Info">
                        <img :src="require(`../assets/img/${item.img1}`)" />
                      </div>

                      <div class="Profile-Details">
                        <h3>{{ item.hading_one }}</h3>
                        <p v-html="item.paragraph_one"></p>

                        <div v-if="item.InstaId_one" class="Feed">
                          <a :href="item.LinkOne">
                            <div class="icon-box">
                              <img src="@/assets/img/insta.svg" />
                            </div>

                            <div class="Feed-details">
                              <h4>{{ item.InstaId_one }}</h4>
                              <h5>{{ item.FollowerK_one }}</h5>
                            </div>
                          </a>
                        </div>
                      </div>
                    </div>

                    <div
                      v-if="item.hading_tow"
                      class="Clippers-Info wow fadeIn"
                      data-wow-delay=".5s"
                    >
                      <div class="Profile-Info">
                        <img :src="require(`../assets/img/${item.img2}`)" />
                      </div>

                      <div class="Profile-Details">
                        <h3>{{ item.hading_tow }}</h3>
                        <p>{{ item.paragraph_tow }}</p>

                        <div v-if="item.InstaId_tow" class="Feed">
                          <a :href="item.LinkTow">
                            <div class="icon-box">
                              <img src="@/assets/img/insta.svg" />
                            </div>

                            <div class="Feed-details">
                              <h4>{{ item.InstaId_tow }}</h4>
                              <h5>{{ item.FollowerK_tow }}</h5>
                            </div>
                          </a>
                        </div>
                      </div>
                    </div>
                  </div>
                </v-carousel-item>
              </v-carousel>
            </v-col>
          </v-row>
        </div>
      </v-container>
    </section>

    <section class="Grooming-business-bg">
      <img src="@/assets/img/PawBg.svg" class="bg-img" />
      <v-container>
        <v-row justify="center">
          <v-col lg="7" md="8" cols="12">
            <div class="Grooming-business-info">
              <div class="Section-Title center">
                <h2 class="main-head wow zoomInDown">
                  Start growing your grooming business for free.
                </h2>
                <p class="wow zoomInDown">
                  All features, no credit card needed.
                </p>
              </div>

              <router-link to="/register">
                <v-btn
                  class="ThemeBtn btn-pink wow rubberBand"
                  data-wow-delay="1.5s"
                  >Try now</v-btn
                >
              </router-link>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </section>

    <section id="Pricing" class="custom-space light-pink">
      <v-container>
        <v-row class="mb-4" justify="center">
          <v-col lg="12">
            <div class="Section-Title center wow fadeInUp">
              <h2 class="sub-head">Plain and simple pricing</h2>
              <p>
                Only pay when you get paid, Only pay 69¢ when a customer is
                checked in. Never pay for <br />no-show and canceled
                appointments. Multiple dogs for one customer counts as a
                single<br />
                appointment. In short, only pay when you get paid!
              </p>
            </div>
          </v-col>
        </v-row>

        <v-row>
          <v-col lg="12">
            <div class="PlanPricing-container">
              <div class="PlansList">
                <ul>
                  <li>
                    <v-icon class="wow rollIn">mdi-check</v-icon> Unlimited SMS
                    messages
                  </li>
                  <li>
                    <v-icon class="wow rollIn">mdi-check</v-icon> Includes
                    automated phone calls.
                  </li>
                  <li>
                    <v-icon class="wow rollIn">mdi-check</v-icon> Keep unlimited
                    customers and pets records.
                  </li>
                  <li>
                    <v-icon class="wow rollIn">mdi-check</v-icon> Smart map
                    scheduling.
                  </li>
                  <li>
                    <v-icon class="wow rollIn">mdi-check</v-icon> Unlimited pet
                    photos
                  </li>
                  <li>
                    <v-icon class="wow rollIn">mdi-check</v-icon> Access to
                    continuous upgrades and features.
                  </li>
                </ul>
              </div>
              <div class="Pricing-Info">
                <h2>69¢</h2>
                <h5>per appointment</h5>
                <p>
                  Volume discounts available starting at 1000 <br />
                  appointments per month.
                </p>
              </div>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </section>

    <section class="light-pink py-3">
      <v-container>
        <v-row>
          <v-col lg="12">
            <div class="FreeTry-container">
              <img src="../assets/img/try-now.png" class="try-now-img" />

              <div class="Info">
                <h3 class="wow fadeInUp">
                  Try Groomer.io for free, for 7 days
                </h3>

                <router-link to="/register">
                  <v-btn class="ThemeBtn wow rubberBand" data-wow-delay="1s"
                    >Try now</v-btn
                  >
                </router-link>
              </div>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </section>

    <section class="custom-space light-pink">
      <v-container>
        <v-row class="">
          <v-col lg="12" class="py-0">
            <div class="Section-Title center">
              <h2 class="sub-head wow fadeInUp">
                How will Groomer.io save your time?
              </h2>
            </div>
          </v-col>
        </v-row>

        <v-row justify="center">
          <v-col lg="12">
            <div class="SaveYour-Time-Conatiner">
              <v-row>
                <v-col lg="12">
                  <div class="MonthlyVisits-Info wow flipInX">
                    <label for="">Enter your average monthly visits</label>
                    <div class="MonthlyVisits-InputBox">
                      <input
                        v-model.number="average_monthly_visits"
                        type="number"
                        min="0"
                        max="9999"
                        placeholder="150"
                        @keydown="limitCharacterLength"
                      />
                    </div>
                  </div>
                </v-col>

                <v-col lg="6" md="6" cols="12">
                  <div class="VisitsResult-Info wow fadeInUp">
                    <div class="Details">
                      <h6>Time savings</h6>
                      <p>Assuming 2 calls per visit, 2 mins each</p>
                    </div>

                    <div class="Quantity">
                      <!--<img src="../assets/img/filter.svg" class="filter-icon">-->
                      <h2>{{ calculation.timeSavingsInHours.toFixed(1) }}hr</h2>
                    </div>
                  </div>
                </v-col>

                <v-col lg="6" md="6" cols="12">
                  <div class="VisitsResult-Info wow fadeInUp">
                    <div class="Details">
                      <h6>Money saved</h6>
                      <p>When paying $15/hr for a receptionist</p>
                    </div>

                    <div class="Quantity">
                      <!--<img src="../assets/img/filter.svg" class="filter-icon">-->
                      <h2>{{ calculation.moneySaved | currency }}</h2>
                    </div>
                  </div>
                </v-col>

                <v-col lg="6" md="6" cols="12">
                  <div class="VisitsResult-Info wow fadeInUp">
                    <div class="Details">
                      <h6>Money earned</h6>
                      <p>Groomer.io's automated sales & marketing</p>
                    </div>

                    <div class="Quantity">
                      <!--<img src="../assets/img/filter.svg" class="filter-icon">-->
                      <h2>{{ calculation.moneyEarned | currency }}</h2>
                    </div>
                  </div>
                </v-col>

                <v-col lg="6" md="6" cols="12">
                  <div class="VisitsResult-Info wow fadeInUp">
                    <div class="Details">
                      <h6>Groomer.io subscription</h6>
                      <p>69¢ per completed visit</p>
                    </div>

                    <div class="Quantity">
                      <!--<img src="../assets/img/filter.svg" class="filter-icon">-->
                      <h2>
                        {{ calculation.groomerioSubscriptionCost | currency }}
                      </h2>
                    </div>
                  </div>
                </v-col>

                <v-col lg="12" cols="12">
                  <div
                    class="
                      VisitsResult-Info
                      Total-VisitsResult-Info
                      wow
                      fadeInUp
                    "
                  >
                    <div class="Details">
                      <h6>Total cash benefit when using Groomer.io</h6>
                    </div>

                    <div class="Quantity">
                      <h2>
                        <span class="green-color">{{
                          calculation.cashBenifit | currency
                        }}</span>
                        monthly
                      </h2>
                    </div>
                  </div>
                </v-col>

                <v-col class="mt-0 mt-md-4" lg="12">
                  <div class="Section-Title center wow fadeInUp">
                    <p>
                      Only pay when you get paid, Only pay 69¢ when a customer
                      is checked in. Never pay for <br />no-show and canceled
                      appointments. Multiple dogs for one customer counts as a
                      single<br />
                      visit. In short, only pay when you get paid!
                    </p>
                  </div>
                </v-col>
              </v-row>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </section>

    <section class="DemoExperience-container">
      <v-container fluid>
        <v-row class="col-reverse-sm">
          <v-col class="pa-0" lg="6" md="6" cols="12">
            <div class="DemoExperience">
              <div class="Section-Title">
                <h2 class="main-head wow bounceInLeft">
                  Get ready for a soothing demo experience.
                </h2>
              </div>

              <div class="PlansList wow bounceInLeft">
                <ul>
                  <li><v-icon>mdi-check</v-icon> All features</li>
                  <li><v-icon>mdi-check</v-icon> No credit card needed</li>
                  <li><v-icon>mdi-check</v-icon> Full support</li>
                  <li><v-icon>mdi-check</v-icon> Guided platform setup</li>
                </ul>
              </div>

              <router-link to="/register">
                <v-btn class="ThemeBtn btn-pink">Try now for free</v-btn>
              </router-link>
            </div>
          </v-col>

          <v-col class="pa-0" lg="6" md="6" cols="12">
            <div class="DemoExperience-Bg">
              <img src="../assets/img/Demo-experience.png" />
            </div>
          </v-col>
        </v-row>
      </v-container>
    </section>

    <section class="custom-space bg-gray Footer-Fit">
      <v-container fluid>
        <v-row>
          <v-col lg="12">
            <div class="Section-Title center">
              <h2 class="sub-head wow fadeInUp">
                Our customers don't bite, they bark.
              </h2>
            </div>
          </v-col>
        </v-row>

        <v-row class="Review-Slider d-none d-md-flex">
          <v-col lg="12">
            <div class="CustomersBite">
              <v-carousel
                hide-delimiters
                :interval="3500"
                :show-arrows="true"
                cycle
                height="auto"
              >
                <v-carousel-item>
                  <div class="CustomerRivew-Slider">
                    <div class="Rivew-InfoBox">
                      <div class="OurCustomers-Info">
                        <div class="Profile">
                          <img src="../assets/img/Shakers-Colors.jpg" />
                        </div>
                        <h3>Shakers Dog wash</h3>
                        <!-- <p>San jose, California</p> -->
                        <span
                          >I spent three months evaluating six different
                          grooming software programs and we decided to switch to
                          Groomer.io. Just to make sure that the program would
                          perform as promised, we ran Groomer.io along with our
                          old software for 60 days. Groomer.io worked as
                          promised and more! We were told it would increase our
                          bookings and I really doubted that would happen. It
                          did!</span
                        >
                      </div>
                    </div>

                    <div class="Rivew-InfoBox">
                      <div class="OurCustomers-Info">
                        <div class="Profile">
                          <img src="../assets/img/profile_westend.png" />
                        </div>
                        <h3>West End Grooming</h3>
                        <!-- <p>San jose, California</p> -->
                        <span
                          >I’ve tried other grooming softwares in the past and
                          none have been as simple and versatile as
                          Groomer.io.</span
                        >
                      </div>
                    </div>

                    <div class="Rivew-InfoBox">
                      <div class="OurCustomers-Info">
                        <div class="Profile">
                          <img src="../assets/img/profile_mypookies.jpg" />
                        </div>
                        <h3>My Pookie's Spaw</h3>
                        <!-- <p>San jose, California</p> -->
                        <span
                          >Groomer.io has made my life and the lives of my
                          customers so much easier! It automatically reminds
                          them of their upcoming appointment and when I'm on my
                          way! They are always telling me that they love my
                          system and how I'm so much more organized and
                          professional than most service based businesses in
                          general. I can't take all the credit because
                          Groomer.io has taken my business to another level. I
                          don't know what I would do without it!</span
                        >
                      </div>
                    </div>

                    <div class="Rivew-InfoBox">
                      <div class="OurCustomers-Info">
                        <div class="Profile">
                          <img src="../assets/img/Wag-n-Wash-Logo.png" />
                        </div>
                        <h3>Wag N Wash, Littleton CO</h3>
                        <!-- <p>San jose, California</p> -->
                        <span
                          >Groomer.io increases revenue by 10% month over month.
                          It pays for itself and then some.</span
                        >
                      </div>
                    </div>
                  </div>
                </v-carousel-item>

                <v-carousel-item>
                  <div class="CustomerRivew-Slider">
                    <div class="Rivew-InfoBox">
                      <div class="OurCustomers-Info">
                        <div class="Profile">
                          <img
                            src="../assets/img/profile_little_creatures.jpg"
                          />
                        </div>
                        <h3>Little Creatures Pet Styling</h3>
                        <!-- <p>San jose, California</p> -->
                        <span
                          >After switching over to Groomer.io my business has
                          become 100% paper free.</span
                        >
                      </div>
                    </div>

                    <div class="Rivew-InfoBox">
                      <div class="OurCustomers-Info">
                        <div class="Profile">
                          <img src="../assets/img/profile_woof.jpg" />
                        </div>
                        <h3>Woofs & Wags, Baltimore, MD</h3>
                        <!-- <p>San jose, California</p> -->
                        <span
                          >Groomer.io helps me keep in contact with all my
                          customers via phone calls and SMS chat.</span
                        >
                      </div>
                    </div>

                    <div class="Rivew-InfoBox">
                      <div class="OurCustomers-Info">
                        <div class="Profile">
                          <img src="../assets/img/profile_camprunamutt.jpg" />
                        </div>
                        <h3>Camp Run-A-Mutt</h3>
                        <!-- <p>San jose, California</p> -->
                        <span
                          >Setting recurring appointments for my clients makes
                          my life so much easier.</span
                        >
                      </div>
                    </div>

                    <div class="Rivew-InfoBox">
                      <div class="OurCustomers-Info">
                        <div class="Profile">
                          <img src="../assets/img/profile_dirty_dogs.jpg" />
                        </div>
                        <h3>Dirty Dogs Groom & Spa</h3>
                        <!-- <p>San jose, California</p> -->
                        <span
                          >Groomer.io saves me dozens of hours per month by
                          automatically contacting customers.</span
                        >
                      </div>
                    </div>
                  </div>
                </v-carousel-item>
              </v-carousel>
            </div>
          </v-col>
        </v-row>

        <!-- For mobile use -->

        <v-row class="d-flex d-md-none">
          <v-col lg="12">
            <div class="CustomersBite">
              <v-carousel
                hide-delimiters
                :interval="3500"
                :show-arrows="true"
                cycle
                height="auto"
              >
                <v-carousel-item>
                  <div class="CustomerRivew-Slider">
                    <div class="Rivew-InfoBox">
                      <div class="OurCustomers-Info">
                        <div class="Profile">
                          <img src="../assets/img/Shakers-Colors.jpg" />
                        </div>
                        <h3>Shakers Dog wash</h3>
                        <!-- <p>San jose, California</p> -->
                        <span
                          >I spent three months evaluating six different
                          grooming software programs and we decided to switch to
                          Groomer.io. Just to make sure that the program would
                          perform as promised, we ran Groomer.io along with our
                          old software for 60 days. Groomer.io worked as
                          promised and more! We were told it would increase our
                          bookings and I really doubted that would happen. It
                          did!</span
                        >
                      </div>
                    </div>
                  </div>
                </v-carousel-item>

                <v-carousel-item>
                  <div class="CustomerRivew-Slider">
                    <div class="Rivew-InfoBox">
                      <div class="OurCustomers-Info">
                        <div class="Profile">
                          <img src="../assets/img/profile_westend.png" />
                        </div>
                        <h3>West End Grooming</h3>
                        <!-- <p>San jose, California</p> -->
                        <span
                          >I’ve tried other grooming softwares in the past and
                          none have been as simple and versatile as
                          Groomer.io.</span
                        >
                      </div>
                    </div>
                  </div>
                </v-carousel-item>

                <v-carousel-item>
                  <div class="CustomerRivew-Slider">
                    <div class="Rivew-InfoBox">
                      <div class="OurCustomers-Info">
                        <div class="Profile">
                          <img src="../assets/img/profile_mypookies.jpg" />
                        </div>
                        <h3>My Pookie's Spaw</h3>
                        <!-- <p>San jose, California</p> -->
                        <span
                          >Groomer.io has made my life and the lives of my
                          customers so much easier! It automatically reminds
                          them of their upcoming appointment and when I'm on my
                          way! They are always telling me that they love my
                          system and how I'm so much more organized and
                          professional than most service based businesses in
                          general. I can't take all the credit because
                          Groomer.io has taken my business to another level. I
                          don't know what I would do without it!</span
                        >
                      </div>
                    </div>
                  </div>
                </v-carousel-item>

                <v-carousel-item>
                  <div class="CustomerRivew-Slider">
                    <div class="Rivew-InfoBox">
                      <div class="OurCustomers-Info">
                        <div class="Profile">
                          <img src="../assets/img/Wag-n-Wash-Logo.png" />
                        </div>
                        <h3>Wag N Wash, Littleton CO</h3>
                        <!-- <p>San jose, California</p> -->
                        <span
                          >Groomer.io increases revenue by 10% month over month.
                          It pays for itself and then some.</span
                        >
                      </div>
                    </div>
                  </div>
                </v-carousel-item>

                <v-carousel-item>
                  <div class="CustomerRivew-Slider">
                    <div class="Rivew-InfoBox">
                      <div class="OurCustomers-Info">
                        <div class="Profile">
                          <img
                            src="../assets/img/profile_little_creatures.jpg"
                          />
                        </div>
                        <h3>Little Creatures Pet Styling</h3>
                        <!-- <p>San jose, California</p> -->
                        <span
                          >After switching over to Groomer.io my business has
                          become 100% paper free.</span
                        >
                      </div>
                    </div>
                  </div>
                </v-carousel-item>

                <v-carousel-item>
                  <div class="CustomerRivew-Slider">
                    <div class="Rivew-InfoBox">
                      <div class="OurCustomers-Info">
                        <div class="Profile">
                          <img src="../assets/img/profile_woof.jpg" />
                        </div>
                        <h3>Woofs & Wags, Baltimore, MD</h3>
                        <!-- <p>San jose, California</p> -->
                        <span
                          >Groomer.io helps me keep in contact with all my
                          customers via phone calls and SMS chat.</span
                        >
                      </div>
                    </div>
                  </div>
                </v-carousel-item>

                <v-carousel-item>
                  <div class="CustomerRivew-Slider">
                    <div class="Rivew-InfoBox">
                      <div class="OurCustomers-Info">
                        <div class="Profile">
                          <img src="../assets/img/profile_camprunamutt.jpg" />
                        </div>
                        <h3>Camp Run-A-Mutt</h3>
                        <!-- <p>San jose, California</p> -->
                        <span
                          >Setting recurring appointments for my clients makes
                          my life so much easier.</span
                        >
                      </div>
                    </div>
                  </div>
                </v-carousel-item>

                <v-carousel-item>
                  <div class="Rivew-InfoBox">
                    <div class="OurCustomers-Info">
                      <div class="Profile">
                        <img src="../assets/img/profile_dirty_dogs.jpg" />
                      </div>
                      <h3>Dirty Dogs Groom & Spa</h3>
                      <!-- <p>San jose, California</p> -->
                      <span
                        >Groomer.io saves me dozens of hours per month by
                        automatically contacting customers.</span
                      >
                    </div>
                  </div>
                </v-carousel-item>
              </v-carousel>
            </div>
          </v-col>
        </v-row>

        <!-- End For mobile use -->

        <!-- <v-row>
          <v-col lg="12">
            <div class="Our-Customers-Container">
              <div class="swiper-container Our-Customers">

                <div class="swiper-wrapper">
                  <div class="swiper-slide wow fadeInUp" data-wow-delay="1s">
                    <div class="OurCustomers-Info">
                      <div class="Profile">
                        <img src="../assets/img/Shakers-Colors.jpg" />
                      </div>
                      <h3>Shakers Dog wash</h3>
                      <span>I spent three months evaluating six different grooming software programs and we decided to switch to Groomer.io. Just to make sure that the program would perform as promised, we ran Groomer.io along with our old software for 60 days. Groomer.io worked as promised and more! We were told it would increase our bookings and I really doubted that would happen. It did!</span>
                    </div>
                  </div>

                  <div class="swiper-slide wow fadeInUp" data-wow-delay="1.2s">
                    <div class="OurCustomers-Info">
                      <div class="Profile">
                        <img src="../assets/img/profile_westend.png">
                      </div>
                      <h3>West End Grooming</h3>
                      <span>I’ve tried other grooming softwares in the past and none have been as simple and versatile as Groomer.io.</span>
                    </div>
                  </div>

                  <div class="swiper-slide wow fadeInUp" data-wow-delay="1.4s">
                    <div class="OurCustomers-Info">
                      <div class="Profile">
                        <img src="../assets/img/profile_mypookies.jpg">
                      </div>
                      <h3>My Pookie's Spaw</h3>
                      <span>Groomer.io has made my life and the lives of my customers so much easier! It automatically reminds them of their upcoming appointment and when I'm on my way! They are always telling me that they love my system and how I'm so much more organized and professional than most service based businesses in general. I can't take all the credit because Groomer.io has taken my business to another level. I don't know what I would do without it!</span>
                    </div>
                  </div>

                  <div class="swiper-slide wow fadeInUp" data-wow-delay="1.6s">
                    <div class="OurCustomers-Info">
                      <div class="Profile">
                        <img src="../assets/img/Wag-n-Wash-Logo.png">
                      </div>
                      <h3>Wag N Wash, Littleton CO</h3>
                      <span>Groomer.io increases revenue by 10% month over month. It pays for itself and then some.</span>
                    </div>
                  </div>

                  <div class="swiper-slide wow fadeInUp" data-wow-delay="1s">
                    <div class="OurCustomers-Info">
                      <div class="Profile">
                        <img src="../assets/img/profile_little_creatures.jpg" />
                      </div>
                      <h3>Little Creatures Pet Styling</h3>
                      <span>After switching over to Groomer.io my business has become 100% paper free.</span>
                    </div>
                  </div>

                  <div class="swiper-slide wow fadeInUp" data-wow-delay="1.2s">
                    <div class="OurCustomers-Info">
                      <div class="Profile">
                        <img src="../assets/img/profile_woof.jpg">
                      </div>
                      <h3>Woofs & Wags, Baltimore, MD</h3>
                      <span>Groomer.io helps me keep in contact with all my customers via phone calls and SMS chat.</span>
                    </div>
                  </div>

                  <div class="swiper-slide wow fadeInUp" data-wow-delay="1.4s">
                    <div class="OurCustomers-Info">
                      <div class="Profile">
                        <img src="../assets/img/profile_camprunamutt.jpg">
                      </div>
                      <h3>Camp Run-A-Mutt</h3>
                      <span>Setting recurring appointments for my clients makes my life so much easier.</span>
                    </div>
                  </div>

                  <div class="swiper-slide wow fadeInUp" data-wow-delay="1.6s">
                    <div class="OurCustomers-Info">
                      <div class="Profile">
                        <img src="../assets/img/profile_dirty_dogs.jpg">
                      </div>
                      <h3>Dirty Dogs Groom & Spa</h3>
                      <span>Groomer.io saves me dozens of hours per month by automatically contacting customers.</span>
                    </div>
                  </div>
                </div>
              </div>

              <div class="Slider-arrow">
                <div class="Arrow swiper-button-prev"><img src="../assets/img/left-arrow.svg"></div>
                <div class="Arrow swiper-button-next"><img src="../assets/img/right-arrow.svg"></div>
              </div>
            </div>
          </v-col>
        </v-row> -->
      </v-container>
    </section>
  </div>
</template>

<script>
import VueSlickCarousel from 'vue-slick-carousel'
import 'vue-slick-carousel/dist/vue-slick-carousel.css'
// optional style for arrows & dots
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'

export default {
  components: { VueSlickCarousel },
  data() {
    return {
      interval: 70000,
      average_monthly_visits: 150,
      Settings: {
        arrows: false,
        centerMode: true,
        dots: false,
        infinite: true,
        slidesToShow: 6,
        slidesToScroll: 1,
        autoplay: true,
        speed: 2500,
        autoplaySpeed: 2500,
        cssEase: 'linear',
      },
      // For mobile
      items: [
        {
          img: 'clippers-img01.png',
          hading: 'Rahanna of Stylish Pooch LLC',
          paragraph:
            'I’ve been using <a href="#">Groomer.io</a> for about 4 years now and it s my go to app. It has made my life so much easier. My favorite part about the app is that it acts as my assistant. It automatically texts my clients the day before every appointment to confirm/decline their grooming appointments. Also with a push of a button, I can notify my clients I am on the way with a call or text. Being a mobile groomer and so busy with appointments, it has really been so helpful over the years!',
          InstaId: '@_stylishpooch_',
          FollowerK: '175K',
          Link: 'https://www.instagram.com/_stylishpooch_/',
        },

        {
          img: 'clippers-img02.png',
          hading: 'Jess Rona',
          paragraph:
            'Groomer.io is the beessssttttttt! After meeting with, and trying various software companies, we ve been using Groomer.io for over a year now. We recently enabled online booking, pay ahead, and deposits for all new clients, and our business is so thankful! We are making more money due to fewer cancellations, quick and efficient check-ins, and check-outs, and less time spent scheduling and rescheduling. The customer service is top notch, and they are very receptive to our feedback. If you accidentally delete an entire client like we have, no prob bob, Groomer io has your back. We are big fans and look forward to seeing how this software grows with our business.',
          InstaId: '@jessronagrooming',
          FollowerK: '202K',
          Link: 'https://www.instagram.com/jessronagrooming/',
        },

        {
          img: 'clippers-img03.png',
          hading: 'Blue Pooch',
          paragraph:
            'The wonderful team at Groomer.io helped made the opening of my new salon a success! Their efficient booking system has made it super easy for all returning and new clients. So many have raved about how easy it to book an appointment! I truly appreciate the wonderful team at Groomer.io, their professionalism, prompt response, and courteous service have made salon life a much positive experience. My favorite feature is the built-in text messaging! It’s helped us stay engaged with all our customers and adds that special personalized touch. I truly am grateful for their presence in my professional life... Doing business has never been so efficient and so pleasant! Thank you to all of you 🤩',
          InstaId: '@arisathegroomer',
          FollowerK: '10.8K',
          Link: 'https://www.instagram.com/arisathegroomer/',
        },

        {
          img: 'katrina.png',
          hading: 'Katrina Short',
          paragraph:
            'Salon life before groomer🐶io I want to say was so stressful! I felt like I was spending so much time at the salon because I had to stop grooming every second to check out a client or take a phone call to book appointments. Felt like it was never-ending. Since switching to groomer🐶io and using it for the last 2 years I will say it dramatically changed the flow of the salon. Clients can book themselves ONLINE!! This saves me time away from the ever-so-busy phones, which allows me to focus on the pets that I’m going on the table. Another stress reliever that this software has, is at the click of a button an automated call/text sends to the pet parent. They get notified their pet is ready and has a link that the owners can pay ahead of pickup arrival! Again saves so much time, I can just check the screen and see that they paid and hand them their dog. It’s an easy, quick pick-up! it’s very easy to use and utilize. Groomer🐶io is very responsive & helpful when it comes to questions. I refer all my followers and friends in the grooming community to this software! I never rep or encouraged anyone anything that I don’t fully stand behind or love. I love this software and the team behind it.',
          InstaId: '@katrina_short ',
          FollowerK: '26K',
          Link: 'https://www.instagram.com/katrina_short/',
        },

        {
          img: 'Gabriel.png',
          hading: 'Gabriel ',
          paragraph:
            'At the GFG pet store everyone LOOOOVES groomer.io, it makes the scheduling so convenient without taking time away from the grooming, fewer phone calls, and distractions throughout the day, so much free time comes from not having to answer the phone. Grateful that an app finally understands the modern groomer needs :), thank you Groomer I.o',
          InstaId: '@gabrielfeitosagroomer',
          FollowerK: '62.1K',
          Link: 'https://www.instagram.com/gabrielfeitosagroomer/',
        },
      ],

      // For mobile end

      items_con: [
        {
          img1: 'clippers-img01.png',
          hading_one: 'Rahanna of Stylish Pooch LLC',
          paragraph_one:
            'I’ve been using <a href="#">Groomer.io</a> for about 4 years now and it s my go to app. It has made my life so much easier. My favorite part about the app is that it acts as my assistant. It automatically texts my clients the day before every appointment to confirm/decline their grooming appointments. Also with a push of a button, I can notify my clients I am on the way with a call or text. Being a mobile groomer and so busy with appointments, it has really been so helpful over the years!',
          InstaId_one: '@_stylishpooch_',
          FollowerK_one: '175K',
          LinkOne: 'https://www.instagram.com/_stylishpooch_/',

          img2: 'clippers-img02.png',
          hading_tow: 'Jess Rona',
          paragraph_tow:
            'Groomer.io is the beessssttttttt! After meeting with, and trying various software companies, we ve been using Groomer.io for over a year now. We recently enabled online booking, pay ahead, and deposits for all new clients, and our business is so thankful! We are making more money due to fewer cancellations, quick and efficient check-ins, and check-outs, and less time spent scheduling and rescheduling. The customer service is top notch, and they are very receptive to our feedback. If you accidentally delete an entire client like we have, no prob bob, Groomer io has your back. We are big fans and look forward to seeing how this software grows with our business.',
          InstaId_tow: '@jessronagrooming',
          FollowerK_tow: '202K',
          LinkTow: 'https://www.instagram.com/jessronagrooming/',
        },

        {
          img1: 'clippers-img03.png',
          hading_one: 'Blue Pooch',
          paragraph_one:
            'The wonderful team at Groomer.io helped made the opening of my new salon a success! Their efficient booking system has made it super easy for all returning and new clients. So many have raved about how easy it to book an appointment! I truly appreciate the wonderful team at Groomer.io, their professionalism, prompt response, and courteous service have made salon life a much positive experience. My favorite feature is the built-in text messaging! It’s helped us stay engaged with all our customers and adds that special personalized touch. I truly am grateful for their presence in my professional life... Doing business has never been so efficient and so pleasant! Thank you to all of you 🤩',
          InstaId_one: '@arisathegroomer',
          FollowerK_one: '10.8K',
          LinkOne: 'https://www.instagram.com/arisathegroomer/',

          img2: 'katrina.png',
          hading_tow: 'Katrina Short',
          paragraph_tow:
            'Salon life before groomer🐶io I want to say was so stressful! I felt like I was spending so much time at the salon because I had to stop grooming every second to check out a client or take a phone call to book appointments. Felt like it was never-ending. Since switching to groomer🐶io and using it for the last 2 years I will say it dramatically changed the flow of the salon. Clients can book themselves ONLINE!! This saves me time away from the ever-so-busy phones, which allows me to focus on the pets that I’m going on the table. Another stress reliever that this software has, is at the click of a button an automated call/text sends to the pet parent. They get notified their pet is ready and has a link that the owners can pay ahead of pickup arrival! Again saves so much time, I can just check the screen and see that they paid and hand them their dog. It’s an easy, quick pick-up! it’s very easy to use and utilize. Groomer🐶io is very responsive & helpful when it comes to questions. I refer all my followers and friends in the grooming community to this software! I never rep or encouraged anyone anything that I don’t fully stand behind or love. I love this software and the team behind it.',
          InstaId_tow: '@katrina_short ',
          FollowerK_tow: '26K',
          LinkTow: 'https://www.instagram.com/katrina_short/',
        },

        {
          img1: 'lastimage.jpg',
          hading_one: 'Gabriel ',
          paragraph_one:
            'At the GFG pet store everyone LOOOOVES groomer.io, it makes the scheduling so convenient without taking time away from the grooming, fewer phone calls, and distractions throughout the day, so much free time comes from not having to answer the phone. Grateful that an app finally understands the modern groomer needs :), thank you Groomer I.o',
          InstaId_one: '@gabrielfeitosagroomer',
          FollowerK_one: '62.1K',
          LinkOne: 'https://www.instagram.com/gabrielfeitosagroomer/',

          // img2: 'img2lastimage562.jpg',
          // hading_tow: 'Dogfatherofharlem ',
          // paragraph_tow:
          //   'At the GFG pet store everyone LOOOOVES groomer.io, it makes the scheduling so convenient without taking time away from the grooming, fewer phone calls, and distractions throughout the day, so much free time comes from not having to answer the phone. Grateful that an app finally understands the modern groomer needs :), thank you Groomer I.o',
          // InstaId_tow: '@dogfatherofharlem',
          // FollowerK_tow: '15.3K',
          // LinkTow: 'https://www.instagram.com/dogfatherofharlem/',
        },
      ],

      slider: [
        'BlueDog.png',
        'BowWow.png',
        'Shakers.png',
        'ClippinTails.png',
        'DogPerfect.png',
        'HairySofa.png',
        'HydroDog.png',
        'KristiFancyK9.png',
        'PerfectPaw.png',
        'PureJoy.png',
        'SDGA.png',
        'Choye.png',
        'Shakers.png',
        'VanderpumpDogs.png',
        'VanityFur.png',
        'VIP.png',
        'WagNWash.png',
        'YourGroomers.png',
      ],
    }
  },

  computed: {
    calculation() {
      const averageMonthlyVisits = Number(this.average_monthly_visits)

      const timeSavingsInHours = (averageMonthlyVisits * 2 * 2) / 60
      const moneyEarned = averageMonthlyVisits * 85 * 0.0384
      const moneySaved = timeSavingsInHours * 15
      const groomerioSubscriptionCost = Math.max(5, averageMonthlyVisits * 0.69)
      const cashBenifit = moneySaved + moneyEarned - groomerioSubscriptionCost

      return {
        timeSavingsInHours,
        moneyEarned,
        moneySaved,
        groomerioSubscriptionCost,
        cashBenifit,
      }
    },

    columns() {
      if (this.$vuetify.breakpoint.xl) {
        return 6
      }

      if (this.$vuetify.breakpoint.lg) {
        return 6
      }

      if (this.$vuetify.breakpoint.md) {
        return 6
      }

      return 6
    },
  },

  methods: {
    limitCharacterLength(e) {
      const deleteKey = 8
      const backspaceKey = 46

      if ([deleteKey, backspaceKey].includes(e.keyCode || e.charCode)) {
        return
      }

      if (e.target.value.length > 4) {
        e.preventDefault()
      }
    },
  },
}
</script>
