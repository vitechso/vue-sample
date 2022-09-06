<template>
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
          <v-col v-for="(title, index) in titles" :key="index" lg="4">
            <router-link to="/blogdetails">
              <div class="InnerBlogGrid">
                <div class="BlogImage">
                  <img src="@/assets/img/dogsimg.png" />
                </div>
                <div class="BottomDetails">
                  <h4>
                    {{ title.title }}
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
        <v-row>
          <v-col lg="12">
            <infinite-loading
              v-if="titles.length"
              spinner="spiral"
              @infinite="infiniteScroll"
            ></infinite-loading>
          </v-col>
        </v-row>
      </v-container>
    </section>
  </div>
</template>

<script>
import axios from 'axios'
import InfiniteLoading from 'vue-infinite-loading'

export default {
  name: 'BlogNew',
  components: {
    InfiniteLoading,
  },
  data() {
    return {
      titles: [],
      page: 1,
    }
  },
  computed: {
    url() {
      return 'https://jsonplaceholder.typicode.com/posts?_page=' + this.page
    },
  },
  created() {
    this.fetchData()
  },

  methods: {
    async fetchData() {
      const response = await axios.get(this.url)
      console.log(this.url)
      this.titles = response.data
    },
    infiniteScroll($state) {
      setTimeout(() => {
        this.page++
        axios
          .get(this.url)
          .then((response) => {
            if (response.data.length > 1) {
              response.data.forEach((item) => this.titles.push(item))
              $state.loaded()
            } else {
              $state.complete()
            }
          })
          .catch((err) => {
            // eslint-disable-next-line no-console
            console.log(err)
          })
      }, 1000)
    },
  },
}
</script>