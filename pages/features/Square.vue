<template>
  <div class="light-pink FitHeader Footer-Fit" style="padding-bottom: 250px">
    <features-section :feature="feature" reversed color="pink">
      <template #example>
        <v-row>
          <v-col>
            <router-link to="/register">
              <v-btn class="ThemeBtn btn-pink" style="width: 100%;max-width:400px;"
                >Start free trial</v-btn
              >
            </router-link>
          </v-col>
        </v-row>
      </template>
    </features-section>
  </div>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const feature = await $content('features', 'square').fetch()

    return {
      feature,
    }
  },
}
</script>

<style>
</style>

<router>
  {
    path: '/features/square'
  }
</router>