<template>
  <section class="custom-space" :class="colorClass">
    <v-container>
      <v-row
        align="center"
        class="mobilereverce"
        :class="{ 'flex-row-reverse': reversed }"
      >
        <v-col lg="6" md="6" cols="12">
          <div>
            <div class="Section-Title">
              <h2
                v-if="feature.heading"
                class="sub-head wow fadeInUp"
              >
                {{ feature.heading }}
              </h2>
              <slot v-else name="heading"></slot>
              <slot name="description">
                <p
                  v-for="paragraph in feature.paragraphs"
                  :key="paragraph"
                  class="dark-p wow fadeInUp"
                >
                  {{ paragraph }}
                </p>
              </slot>
            </div>

            <div class="NewsLetter-Group wow fadeInUp">
              <slot name="example"></slot>
            </div>
            <div v-if="feature.faqs.length > 0" class="divider"></div>

            <slot name="faq">
              <div
                v-for="faq in feature.faqs"
                :key="faq.question"
                class="Question-Tag wow fadeInUp"
              >
                <h3>{{ faq.question }}</h3>
                <p>{{ faq.answer }}</p>
              </div>
            </slot>
          </div>
        </v-col>
        <component
          :is="feature.image.value"
          v-if="feature.image.component === true"
          :on-color="color"
        ></component>
        <slot v-else name="image"></slot>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  props: {
    feature: {
      type: Object,
      required: true,
    },
    reversed: {
      type: Boolean,
      required: false,
      default: false,
    },
    color: {
      type: String,
      required: false,
      default: 'white',
    },
  },
  computed: {
    colorClass() {
      return {
        white: null,
        blue: 'bg-gray',
        pink: 'light-pink',
      }[this.color];
    }
  }
}
</script>

<style>
</style>