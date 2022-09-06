<template>
  <!-- <div class="FitHeader page Footer-Fit">
    <v-container fluid class="light-pink">
      <v-container class="heading">
        <img
          class="hero-image"
          :src="post.image"
          :alt="`${post.title} image`"
        />
        <h1>{{ post.title }}</h1>
        <p>{{ post.description }}</p>
        <author :author="author"></author>
      </v-container>
    </v-container>
    <v-container class="content">
      <nuxt-content :document="post"></nuxt-content>
    </v-container>
  </div> -->

  <div>
    <section class="light-pink FitHeader">
      <v-container>
        <v-row align="center" justify="center">
          <v-col lg="5">
            <img
              :src="require(`@/assets/img/${post.image || 'DetailsDog.png'}`)"
              class="MainBanner"
            />

            <v-row align="center" justify="center">
              <v-col>
                <div class="BlogDetail">
                  <h2>{{ post.title }}</h2>
                  <p>{{ post.description }}</p>
                  <author :author="author" :post="post"></author>
                </div>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-container>
    </section>

    <section>
      <v-container>
        <v-row align="center" justify="center">
          <v-col lg="5">
            <nuxt-content :document="post"></nuxt-content>
          </v-col>
        </v-row>
      </v-container>
    </section>

    <section class="light-pink Footer-Fit pt-10">
      <v-container>
        <v-row>
          <v-col lg="12">
            <div class="AlsoLike">
              <h2>You may also like</h2>
            </div>
          </v-col>
        </v-row>

        <v-row class="mt-5">
          <v-col lg="4">
            <router-link to="/blogdetails">
              <div class="InnerBlogGrid">
                <div class="BlogImage">
                  <img src="@/assets/img/dogsimg.png" />
                </div>
                <div class="BottomDetails">
                  <h4>
                    Opening your own dog grooming business have naver been
                    easier.
                  </h4>
                  <div class="BottomBar">
                    <span>01/01/2022</span>
                    <span>Reading time: 5min</span>
                  </div>
                </div>
              </div>
            </router-link>
          </v-col>
          <v-col lg="4">
            <router-link to="/blogdetails">
              <div class="InnerBlogGrid">
                <div class="BlogImage">
                  <img src="@/assets/img/dogsimg.png" />
                </div>
                <div class="BottomDetails">
                  <h4>
                    Opening your own dog grooming business have naver been
                    easier.
                  </h4>
                  <div class="BottomBar">
                    <span>01/01/2022</span>
                    <span>Reading time: 5min</span>
                  </div>
                </div>
              </div>
            </router-link>
          </v-col>
          <v-col lg="4">
            <router-link to="/blogdetails">
              <div class="InnerBlogGrid">
                <div class="BlogImage">
                  <img src="@/assets/img/dogsimg.png" />
                </div>
                <div class="BottomDetails">
                  <h4>
                    Opening your own dog grooming business have naver been
                    easier.
                  </h4>
                  <div class="BottomBar">
                    <span>01/01/2022</span>
                    <span>Reading time: 5min</span>
                  </div>
                </div>
              </div>
            </router-link>
          </v-col>
        </v-row>
      </v-container>
    </section>
  </div>
</template>

<script>
import Author from '~/components/Author.vue'
export default {
  components: { Author },
  async asyncData({ $content, params }) {
    const post = await $content('blog', params.slug).fetch()
    const author = await $content('authors', post.author ?? 'groomerio').fetch()

    return {
      post,
      author,
    }
  },
}
</script>

<style scoped>
.page {
}
.content {
  max-width: 960px;
  margin: 0 auto;
}
.heading {
  max-width: 960px;
  margin: 0 auto;
}
.hero-image {
  width: 100%;
}
</style>