<template>
  <div id="Features-Page">
    <section class="Feaures-banner light-pink Bottom-sky FitHeader">
      <v-container>
        <v-row>
          <v-col lg="12">
            <div class="Banner-Details text-center">
              <h1 class="wow zoomInDown">
                Everything your storefront grooming <br />business needs.
              </h1>
              <h5 class="wow zoomInDown" data-wow-delay="0.3s">
                And a few other features.
              </h5>
            </div>
          </v-col>
        </v-row>
      </v-container>

      <img src="@/assets/img/Union-bg.png" class="Union-bg" />
      <img src="@/assets/img/sky-bg.png" class="sky-bg pos" />
    </section>

    <features-section
      :feature="features['ready-for-pickup']"
      :reversed="true"
      color="white"
    >
      <template #example>
        <features-phone-example
          endpoint="/api/public/v1/automations/pick-up"
          button-title="Hear for yourself"
        ></features-phone-example>
      </template>
    </features-section>

    <features-section
      :feature="features['unlimited-sms']"
      :reversed="false"
      color="blue"
    >
    </features-section>

    <features-section
      :feature="features['booking-styles']"
      :reversed="true"
      color="pink"
    ></features-section>

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
                  data-wow-delay="1s"
                  >Try now</v-btn
                >
              </router-link>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </section>

    <features-section
      :feature="features['mass-messaging']"
      :reversed="true"
      color="white"
    ></features-section>

    <features-section
      :feature="features['online-booking']"
      :reversed="false"
      color="blue"
    >
    <template #example>
        <v-btn
          type="submit"
          :href="$config.onlineBookingURL"
          target="_blank"
          class="ThemeBtn wow fadeInUp"
          data-wow-delay="2s"
          >See for yourself</v-btn
        >
      </template>
    </features-section>

    <features-section
      :feature="features['online-requesting']"
      :reversed="true"
      class="Footer-Fit"
      color="pink"
    >
      <template #example>
        <v-btn
          type="submit"
          :href="$config.onlineRequestURL"
          target="_blank"
          class="ThemeBtn wow fadeInUp"
          data-wow-delay="2s"
          >See for yourself</v-btn
        >
      </template>
    </features-section>
  </div>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const features = await $content('features').fetch()
    const featuresKeyedByIdentifier = {}

    features.forEach((feature) => {
      featuresKeyedByIdentifier[feature.identifier] = feature
    })

    return {
      features: featuresKeyedByIdentifier,
    }
  },
}
</script>

