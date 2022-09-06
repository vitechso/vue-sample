<template>
  <div class="light-pink FitHeader Footer-Fit" style="padding-bottom: 250px">
    <features-section :feature="feature" reversed color="pink">
      <template #example>
        <v-row>
          <v-col>
            <v-btn
              type="submit"
              :href="$config.intakePageURL"
              target="_blank"
              class="ThemeBtn btn-blue"
              data-wow-delay="2s"
              style="width: 100%;max-width:400px;"
              >See an example</v-btn
            >
            <div class="divider"></div>
            <router-link to="/register">
              <v-btn class="ThemeBtn btn-pink" style="width: 100%;max-width:400px;"
                >Start free trial</v-btn
              >
            </router-link>
          </v-col>
        </v-row>
      </template>
    </features-section>
    <div v-if="influencer" class="d-md-flex Testimonial">
      <v-row justify="center">
        <v-col class="mx-4" lg="6" md="8">
          <influencer :influencer="influencer"></influencer>
        </v-col>
      </v-row>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData({ $content, query }) {
    const feature = await $content('features', 'intake-page').fetch()
    const influencer = query.influencer
      ? await $content('influencers', query.influencer).fetch()
      : null

    return {
      feature,
      influencer,
    }
  },
}
</script>

<style>
</style>

<router>
  {
    path: '/features/intake-page'
  }
</router>