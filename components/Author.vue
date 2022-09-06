<template>
  <div class="BlogUserDetails">
    <div class="userImg">
      <img :src="require(`@/assets/img/${author.image}`)" />
    </div>
    <div class="UserNameH">
      <h4>{{author.name}}</h4>
      <p>{{post.createdAt | date}}<span v-if="post.duration">, {{post.duration}} MIN READ</span></p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    author: {
      type: Object,
      required: true,
    },
    post: {
      type: Object,
      required: true,
    }
  }
}
</script>