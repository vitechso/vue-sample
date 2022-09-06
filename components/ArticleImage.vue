<template>
  <div class="BannerMiddle">
    <img :src="imgSrc()" :alt="alt" class="article-image" />
  </div>
</template>

<script>
export default {
  props: {
    src: {
      type: String,
      required: true,
    },
    alt: {
      type: String,
      required: true,
    },
  },
  methods: {
    imgSrc() {
      try {
        return require(`~/assets/blog/images/${this.src}`)
      } catch (error) {
        return null
      }
    },
  },
}
</script>

<style>
</style>