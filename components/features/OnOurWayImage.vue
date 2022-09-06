<template>
  <v-col lg="6" md="6" cols="12">
    <div class="Banner-Circle-Info PickupPhoneCall-Comments-Info">
      <div class="Inner-Circle-Info">
        <div class="Img-Info wow fadeIn"
          :style="{backgroundColor: color}"
        ></div>

        <div class="PhoneCallComment-Info">
          <div class="Inner-Comment wow fadeInUp">
            <div class="Text-Box wow fadeIn" data-wow-delay="1.5s">
              <h5>
                We are on our way for our appointment at 4! See you there!
              </h5>
            </div>

            <div class="sound-reflection wow fadeInUp" data-wow-delay="1s">
              <img src="@/assets/img/sound-reflection.svg" />
            </div>
          </div>

          <div class="Comment-Profile wow fadeInUp" data-wow-delay=".5s">
            <div class="Img-Box">
              <img src="@/assets/img/cmnt-img01.png" />
            </div>
            <div class="Call-Icon">
              <img src="@/assets/img/call.svg" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </v-col>
</template>

<script>
import ColorableImage from "@/mixins/ColorableImage";

export default {
    mixins: [ColorableImage]    
}
</script>

<style>
</style>