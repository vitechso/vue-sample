<template>
  <div class="Clippers-Container">
    <div class="Clippers-Info wow fadeIn">
      <div class="Profile-Info">
        <img :src="require(`../assets/img/${influencer.img}`)" />
      </div>

      <div class="Profile-Details">
        <h3>{{ influencer.name }}</h3>
        <!-- eslint-disable vue/no-v-html -->
        <p v-html="influencer.review"></p>
        <!--eslint-enable-->

        <div v-if="influencer.instagram.handle" class="Feed">
          <a :href="influencer.instagram.link">
            <div class="icon-box">
              <img src="@/assets/img/insta.svg" />
            </div>

            <div class="Feed-details">
              <h4>{{ influencer.instagram.handle }}</h4>
              <h5>{{ influencer.instagram.followers }}</h5>
            </div>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    influencer: {
      type: Object,
      required: true,
    },
  },
}
</script>

<style>
</style>