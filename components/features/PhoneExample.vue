<template>
  <div class="NewsLetter-Group wow fadeInUp">
    <phone-input v-model="phone" class="custom-input"></phone-input>
    <v-btn
      :disabled="phone.length == 0"
      type="submit"
      class="ThemeBtn wow fadeInUp"
      @click="commit"
      >{{ buttonTitle }}</v-btn
    >
  </div>
</template>

<script>
export default {
  props: {
    endpoint: {
      type: String,
      required: true,
    },
    buttonTitle: {
      type: String,
      required: false,
      default: 'Try Now',
    },
  },
  data() {
    return {
      phone: '',
      companies: [
        'Pampered Pets',
        'The Pawfectionist, Inc.',
        'Paws To Perfection',
        'Pampered Pooch',
        'Whisker Lickin’ Good',
        'Furry Goodness',
        'Pawdicure and Pedicure',
        'Posh Pets Boutique',
        'Doggies Delight',
        'Dog Groomers Inc.',
        'Pawfections',
        'Station Puppy',
        'Alpha Dog Grooming',
      ],
    }
  },
  methods: {
    commit() {
      const companyIndex = Math.floor(Math.random() * this.companies.length)

      this.$axios
        .post(this.endpoint, {
          phone: this.phone,
          company_name: this.companies[companyIndex],
        })
        .then((res) => {
          if (res.status === 200) {
            this.$toast.success('You will here from us soon!')
            this.phone = ''
          } else {
            this.$toast.error('Something went wrong!')
          }
        })
    },
  },
}
</script>

<style>
</style>