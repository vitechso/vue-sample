<template>
  <h2 class="sub-head wow fadeInUp">
    <span class="circled" :style="{filter: `contrast(${contrast}%)`, backgroundSize: size}">Unlimited</span>
    SMS messaging
  </h2>
</template>
<script>
export default {
    props: {
        contrast: { type: Number, required: false, default: 100},
        size: {type: String, requried: false, default: '142px 60px'}
    }
}
</script>
<style scoped>
.circled {
    position: relative;
    background-color: transparent;
}
.circled::before {
    content: ' ';
    position: absolute;
    top: -9px;
    width: 182px;
    height: 74px;
    background-size: 142px 60px;
    z-index: -1;
    background-image: url("@/assets/img/text-circle-gray.svg");
}
</style>