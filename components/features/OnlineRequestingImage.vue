<template>
  <v-col lg="6" md="6" sm="6" cols="12">
    <div class="OnlineRequesting-Info">
      <div class="Back-Circle wow fadeInUp" data-wow-delay="1s"
        :style="{backgroundColor: color}"
      ></div>
      <div class="Requesting-Info-Detals wow fadeIn" data-wow-delay="0.5s"
        :style="{backgroundColor: color}"
      >
        <div class="icon-box">
          <img src="@/assets/img/paw.png" />
        </div>

        <h2>Paw Paradise</h2>

        <div class="NewsLetter-Group">
          <v-text-field placeholder="Your phone number" class="custom-input" value="555-555-5555" disabled></v-text-field>
          <div class="ThemeBtn btn-pink wow fadeInUp" data-wow-delay="2s">Request</div>
        </div>
      </div>

      <div class="Profile-Icon wow fadeInUp">
        <img src="@/assets/img/request-call-paw.png" />
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