<template>
  <v-col lg="6" md="6" sm="6" cols="12">
    <div class="Banner-Circle-Info PickupPhoneCall-Comments-Info">
      <div class="Inner-Circle-Info">
        <div class="PetAvater-Info wow fadeInUp arrow"
          :class="`arrow-${colorName}`"
          :style="{backgroundColor: color}"
        >
          <!-- <img class="Downarrow" src="@/assets/img/arrowdown.png" :style="`filter: opacity(0.5) drop-shadow(0 0 0 ${color}); saturate(1000%)`" /> -->
        </div>

        <div class="AllPets">
          <div class="MassPetRow wow flipInX" data-wow-delay="1s">
            <img src="@/assets/img/unsplash_N04FIfHhv_k.png" />
            <img
              class="highlight"
              src="@/assets/img/unsplash_2l0CWTpcChI.png"
            />
            <img src="@/assets/img/unsplash_G8cB8hY3yvU.png" />
          </div>
          <div class="MassPetRowTow wow flipInX" data-wow-delay="1s">
            <img src="@/assets/img/unsplash_uhnbTZC7N9k.png" />
            <img src="@/assets/img/unsplash_Sg3XwuEpybU.png" />
            <img src="@/assets/img/unsplash_2s6ORaJY6gI.png" />
            <img src="@/assets/img/unsplash_9UUoGaaHtNE.png" />
          </div>
          <div class="MassPetRowThree wow flipInX" data-wow-delay="1s">
            <img src="@/assets/img/unsplash_OzAeZPNsLXk.png" />
            <img src="@/assets/img/unsplash_mx0DEnfYxic.png" />
            <img src="@/assets/img/unsplash_FilM6ng7VGQ.png" />
          </div>
        </div>

        <div class="useravater wow fadeInUp" data-wow-delay="0.5s">
          <div class="innerAvater">
            <img src="@/assets/img/cmnt-img01.png" />
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

<style scoped>
.arrow::before {
  content: "\25bc";
  position: absolute;
  top: 208px;
  left: 145px;
}

.arrow-pink.arrow::before {
  color: rgb(255, 234, 232);
}
.arrow-blue.arrow::before {
  color: #F4F6FE;
}
.arrow-white.arrow::before {
  color: white;
}
</style>