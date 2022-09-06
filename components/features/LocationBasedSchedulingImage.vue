<template>
  <v-col lg="6" md="6" sm="6" cols="12" class="wow fadeInUp">
    <div class="Banner-Circle-Info PickupPhoneCall-Comments-Info">
      <div class="Inner-Circle-Info">
        <div class="Img-Info wow fadeInUp" data-wow-delay=".5s"
        :style="{backgroundColor: color}"
        ></div>
        <div class="Mapmobileview wow fadeInUp" data-wow-delay="1s">
          <img alt="MapView" src="@/assets/img/Object.svg" class="bg-img" />
        </div>
        <div class="harry">
          <div class="dogimg">
            <img
              alt="MapView"
              src="@/assets/img/unsplash_mx0DEnfYxic.png"
              class="bg-img"
            />
          </div>
          <div class="timehayys">
            <h5>6:30 PM</h5>
            <h3>Harry</h3>
          </div>
          <img
            alt="MapView"
            src="@/assets/img/arrowdownin.svg"
            class="downimg"
          />
        </div>

        <div class="Daisy">
          <div class="dogimg">
            <img
              alt="MapView"
              src="@/assets/img/unsplash_2s6ORaJY6gI.png"
              class="bg-img"
            />
          </div>
          <div class="timehayys">
            <h5>6:30 PM</h5>
            <h3>Daisy</h3>
          </div>
          <img
            alt="MapView"
            src="@/assets/img/arrowdownin.svg"
            class="downimg"
          />
        </div>

        <div class="Preston">
          <div class="dogimg">
            <img
              alt="MapView"
              src="@/assets/img/unsplash_G8cB8hY3yvU.png"
              class="bg-img"
            />
          </div>
          <div class="timehayys">
            <h5>6:30 PM</h5>
            <h3>Preston</h3>
          </div>
          <img
            alt="MapView"
            src="@/assets/img/arrowdownin.svg"
            class="downimg"
          />
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