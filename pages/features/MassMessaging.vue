<template>
  <div class="light-pink FitHeader Footer-Fit">
    <features-section :feature="feature" reversed color="pink">
      <template #example>
        <router-link to="/register">
          <v-btn class="ThemeBtn btn-blue">Try for free</v-btn>
        </router-link>
      </template>
    </features-section>
  </div>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const feature = await $content('features', 'mass-messaging').fetch()

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
    path: '/features/mass-message'
  }
</router>