<template>
  <v-app>
    <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
      class="DrawerSlide"
      width="100%"
    >
      <v-list>
        <div class="BrandLogo">
          <router-link class="navbar-brand" to="/">
            <img alt="Vue logo" src="@/assets/logo/mobilelogo.svg" />
          </router-link>

          <div class="closebtn" @click.stop="drawer = !drawer">
            <img alt="closelogo" src="@/assets/img/close-outline.svg" />
          </div>
        </div>

        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>

        <div class="Header-SideNavBtns">
          <router-link to="/register">
            <v-btn class="ThemeBtn btn-pink">Sign up</v-btn>
          </router-link>

          <a target="_blank" href="https://groomer.io/login">
            <v-btn class="ThemeBtn btn-pink">Log in</v-btn>
          </a>
        </div>
      </v-list>
      <img
        alt="Vuelogo"
        src="@/assets/img/PawelementR.png"
        class="petfootright"
      />
      <img
        alt="Vuelogo"
        src="@/assets/img/PawelementL.png"
        class="petfootleft"
      />
    </v-navigation-drawer>

    <v-app-bar class="TopHeader">
      <v-container>
        <v-row align="center">
          <v-app-bar-nav-icon
            class="ToggleMenu"
            @click.stop="drawer = !drawer"
          />
          <v-col cols="12" class="TopNav">
            <div class="Navigation wow fadeIn" data-wow-delay="0.2s">
              <div class="BrandLogo">
                <router-link class="navbar-brand" to="/">
                  <img alt="Vue logo" src="@/assets/logo/logo.svg" />
                </router-link>
              </div>

              <div class="Mainmenu">
                <ul class="navbar-nav me-auto">
                  <li v-for="(item, i) in items" :key="i" router exact>
                    <router-link :to="item.to">
                      {{ item.title }}
                    </router-link>
                  </li>
                </ul>
              </div>

              <div class="Header-Btns">
                <a target="_blank" href="https://groomer.io/login">
                  <v-btn class="ThemeBtn btn-pink d-none d-md-block"
                    >Log in</v-btn
                  >
                </a>

                <router-link to="/register">
                  <v-btn class="ThemeBtn SignUp-btn">Sign up</v-btn>
                </router-link>
              </div>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </v-app-bar>

    <v-main>
      <Nuxt />
    </v-main>

    <section class="Main-Footer-Container">
      <img src="@/assets/img/sky-bg.png" class="sky-bg" />
      <v-footer class="Main-Footer">
        <v-container>
          <v-row justify="center" align="center">
            <v-col cols="12" sm="11" md="11" lg="11">
              <div class="FooterCard">
                <div class="BrandLogo">
                  <router-link to="/">
                    <img alt="Vue logo" src="@/assets/logo/logo.svg" />
                  </router-link>
                </div>

                <div class="Right-Info">
                  <h5>Start growing your grooming business</h5>
                  <router-link to="/register">
                    <v-btn class="ThemeBtn btn-pink">Try for free</v-btn>
                  </router-link>
                </div>
              </div>

              <div class="divider"></div>

              <div class="FooterNav-container">
                <ul class="Inline-social">
                  <li>
                    <a href="https://www.facebook.com/groomerio/"
                      ><img alt="Vue logo" src="@/assets/img/facebook.svg"
                    /></a>
                  </li>
                  <li>
                    <a href="https://twitter.com/groomerio"
                      ><img alt="Vue logo" src="@/assets/img/twiter.svg"
                    /></a>
                  </li>
                  <li>
                    <a href="https://www.instagram.com/groomer.io/"
                      ><img alt="Vue logo" src="@/assets/img/instagram.svg"
                    /></a>
                  </li>
                </ul>
              </div>
            </v-col>
          </v-row>
        </v-container>
      </v-footer>
    </section>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      items: [
        {
          title: 'Salon',
          to: '/storefront',
        },
        {
          title: 'Mobile',
          to: '/mobile',
        },
        {
          title: 'Pricing',
          to: '/#Pricing',
        },
        {
          title: 'FAQs',
          to: '/faq',
        },
        // {
        //   title: 'Blog',
        //   to: '/blognew',
        // },
      ],
      title: 'Groomer',
    }
  },
}
</script>
