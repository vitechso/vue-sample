<template>
  <v-col lg="6" md="6" cols="12" class="wow lightSpeedInRight">
    <div class="Banner-Circle-Info Messaging-Comments-Info">
      <div class="Inner-Circle-Info">
        <div class="Img-Info wow fadeIn" data-wow-delay="1s"
          :style="{backgroundColor: color}"
        >
          <img src="@/assets/img/iPhoneX.png" />
        </div>

        <div class="Comment-Info wow lightSpeedIn" data-wow-delay="1.5s">
          <div class="Img-Box">
            <img src="@/assets/img/cmnt-img01.png" />
          </div>
          <div class="Comment-details">
            <h5>
              Hi Monica, just letting you know that Diego will be ready 15 mins
              earlier!
            </h5>
          </div>
        </div>

        <div
          class="Comment-Info comment-2 wow lightSpeedIn"
          data-wow-delay="1.5s"
        >
          <div class="Img-Box">
            <img src="@/assets/img/cmnt-img02.png" />
          </div>
          <div class="Comment-details">
            <h5>Great, will pick him up asap!</h5>
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