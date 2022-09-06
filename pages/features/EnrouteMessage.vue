<template>
  <div class="light-pink FitHeader Footer-Fit" style="padding-bottom:250px;">
    <features-section :feature="feature" reversed color="pink">
      <template #example>
        <div>
          <features-phone-example
            endpoint="/api/public/v1/automations/on-our-way"
            button-title="Hear for yourself"
          ></features-phone-example>
          <div class="divider"></div>
          <router-link to="/register">
            <v-btn class="ThemeBtn btn-pink" style="width:100%">Start free trial</v-btn>
          </router-link>
        </div>
      </template>
    </features-section>
  </div>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const feature = await $content('features', 'on-our-way').fetch()

    return {
      feature,
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
    path: '/features/enroute-message'
  }
</router>