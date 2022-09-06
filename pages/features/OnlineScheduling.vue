<template>
  <div class="FitHeader light-pink">
    <features-section
      :feature="features['online-booking']"
      reversed
      color="pink"
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

    <section class="Grooming-business-bg">
      <img src="@/assets/img/PawBg.svg" class="bg-img" />
      <v-container>
        <v-row justify="center">
          <v-col lg="7" md="8" cols="12">
            <div class="Grooming-business-info">
              <div class="Section-Title center">
                <h2 class="main-head wow zoomInDown">
                  Everybody has a different style.
                </h2>
                <p class="wow zoomInDown">
                  Pick the online scheduling style that works best for you and your clients.
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
      :feature="features['online-requesting']"
      color="blue"
      class="Footer-Fit"
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
    const features = await $content('features')
      .where({ identifier: { $in: ['online-booking', 'online-requesting'] } })
      .fetch()

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

<style scoped>
li {
  background-color: white;
  width: 100%;
  padding: 24px;
  margin-bottom: 24px;
  border-radius: 20px;
}
</style>

<router>
  {
    path: '/features/online-scheduling'
  }
</router>