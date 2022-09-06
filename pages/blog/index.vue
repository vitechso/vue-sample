<template>
  <!-- <div class="FitHeader light-pink Footer-Fit">
    <v-container class="grid">
      <template v-for="post in posts">
        <nuxt-link :key="post.slug" :to="post.path">
          <v-card class="post pa-4">
            <img :src="post.image" />
            <h1>{{ post.title }}</h1>
          </v-card>
        </nuxt-link>
      </template>
    </v-container>
  </div> -->

  <div>
    <section class="custom-space light-pink Footer-Fit FitHeader BlogPage">
      <img src="@/assets/img/Union-bg.png" class="Union-bg" />
      <v-container>
        <v-row align="center">
          <v-col lg="12">
            <div class="Section-Title center">
              <h2 class="sub-head wow zoomInDown BlogTitle">
                The Groomer.io blog
              </h2>
              <h6 class="wow zoomInDown BlogSubTitle">
                Latest news form the Isle of Dogs (???)
              </h6>
            </div>
          </v-col>
        </v-row>

        <v-row>
          <v-col v-for="(post, index) in posts" :key="index" lg="4">
            <nuxt-link :key="post.slug" :to="post.path">
              <div class="InnerBlogGrid">
                <div class="BlogImage">
                  <img src="@/assets/img/dogsimg.png" />
                </div>
                <div class="BottomDetails">
                  <h4>
                    {{ post.title }}
                  </h4>
                  <div class="BottomBar">
                    <span>{{ post.createdAt | date }}</span>
                    <span v-if="post.duration">Reading time: {{ post.duration }}min</span>
                  </div>
                </div>
              </div>
            </nuxt-link>
          </v-col>
          <!-- <infinite-loading
            v-if="posts.length"
            spinner="spiral"
            @infinite="infiniteScroll"
          ></infinite-loading> -->
        </v-row>
      </v-container>
    </section>
  </div>
</template>

<script>
export default {
  async asyncData({ $content, query, error, $config }) {
    if ($config.showBlog !== true) {
      await error({statusCode: 404 });
    }

    const perPage = 10;

    const posts = await $content('blog')
      .sortBy('createdAt', 'desc')
      .limit(perPage)
      .skip(perPage * (Number(query.page ?? 1) - 1))
      .fetch();

    return {
      posts,
    }
  },
}
</script>

<style scoped>
.grid {
  display: grid;
  grid-template-columns: 1fr;
  column-gap: 24px;
  row-gap: 24px;
}

@media screen and (min-width: 960px) {
  .grid {
    grid-template-columns: 1fr 1fr;
  }
}

@media screen and (min-width: 1264px) {
  .grid {
    grid-template-columns: 1fr 1fr 1fr;
  }
}

.post {
  height: 200px;
}
</style>