<template>
  <v-col cols="12" sm="6" md="6" lg="6" class="">
    <div class="Banner-Circle-Info">
      <div class="Inner-Circle-Info">
        <div class="Img-Info wow fadeIn" data-wow-delay="1s">
          <img src="@/assets/img/banner-img.png" />
        </div>

        <div class="wow lightSpeedIn" data-wow-delay="1.5s">
          <div class="Tip-Info">
            <div class="Titles">
              <h4>Add a tip?</h4>
              <p>Happy with your pets fresh look? Say thanks to the Groomer.</p>
            </div>

            <div class="Tip-grid">
              <div class="Grid-box">
                <h3>15%</h3>
                <p>$30.15</p>
              </div>

              <div class="Grid-box">
                <h3>20%</h3>
                <p>$45.70</p>
              </div>

              <div class="Grid-box active">
                <h4>Average tip</h4>
                <h3>22.2%</h3>
                <p>$60.12</p>
              </div>

              <div class="Grid-box">
                <h3>25%</h3>
                <p>$60.12</p>
              </div>
            </div>

            <div class="Tip-Btns">
              <a href="#">I’ll tip in person</a>
              <a href="#">Custom amount</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </v-col>
</template>

<script>
import ColorableImage from '@/mixins/ColorableImage'

export default {
  mixins: [ColorableImage],
}
</script>

<style>
</style>