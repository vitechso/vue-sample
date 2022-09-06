<template>
  <v-col lg="6" md="6" sm="6" cols="12" class="wow fadeInUp">
    <div class="Banner-Circle-Info PickupPhoneCall-Comments-Info">
      <div class="Inner-Circle-Info">
        <div class="Img-Info wow fadeInUp" data-wow-delay=".5s"
            :style="{backgroundColor: color}"
        ></div>
        <div class="MapView wow fadeInUp" data-wow-delay="1s">
          <img alt="MapView" src="@/assets/img/mapview.png" class="bg-img" />
        </div>
        <div class="SlotAvailable wow lightSpeedIn" data-wow-delay="1s">
          <div class="BeckyRow">
            <div class="BlockOne">
              <p>Becky</p>
              <p class="Slotactive">1/5</p>
            </div>
            <div class="BlockOne">
              <p>Jackie</p>
              <p class="Slotactive">1/2</p>
            </div>
            <div class="BlockOne">
              <p>Tom</p>
              <p class="Slotactivewithout">1/1</p>
            </div>
          </div>

          <div class="SlotTime">
            <div class="TimeNote">
              <span>9:00</span>
            </div>
            <div class="SlotsA">
              <p>1 Slot Available</p>
            </div>
          </div>

          <div class="SlotTime">
            <div class="TimeNote">
              <span>10:00</span>
            </div>
            <div class="SlotsA">
              <p>3 Slot Available</p>
            </div>
          </div>

          <div class="SlotTime">
            <div class="TimeNote">
              <span>11:00</span>
            </div>
            <div class="SlotsA">
              <p>No room Available</p>
            </div>
          </div>
        </div>

        <div class="PangoRoger wow lightSpeedIn" data-wow-delay="1s">
          <div class="DogUserm">
            <img src="@/assets/img/DogImage.png" class="doguser" />
          </div>
          <div class="ConfirmBox">
            <span>Confirmed</span>
          </div>

          <div class="NameRow">
            <div class="petname">
              <h4>Pongo</h4>
            </div>
            <div class="hours">
              <h5>1.5 hr</h5>
            </div>
          </div>
          <div class="RogerText">
            <p>Roger Wright</p>
            <p>Dalmatian</p>
            <p>Full Groom</p>
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