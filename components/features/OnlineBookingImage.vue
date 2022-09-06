<template>
  <v-col lg="6" md="6" sm="12" cols="12" class="wow lightSpeedInRight">
    <div class="OnlineBooking-Details wow fadeIn">
      <div class="Pets-Type wow lightSpeedIn" data-wow-delay="1s">
        <h5>What type of pet do you have?</h5>

        <ul class="Pets-Info">
          <li>
            <input id="Dog" type="radio" name="Pets" checked />
            <label for="Dog">
              <div class="icon-box">
                <img src="@/assets/img/dogs.svg" />
              </div>
              <p>Dog</p>
            </label>
          </li>

          <li>
            <input id="Cat" type="radio" name="Pets" />
            <label for="Cat">
              <div class="icon-box">
                <img src="@/assets/img/cats.svg" />
              </div>
              <p>Cat</p>
            </label>
          </li>
        </ul>
      </div>

      <div class="Teds-Breed wow fadeInUp" data-wow-delay="1s">
        <h5>What is Ted’s breed?</h5>
        <div class="SearchBox">
          <v-text-field type="text" class="custom-input" disabled></v-text-field>
          <v-icon>mdi-magnify</v-icon>
        </div>
        <p>For mixed breed, select multiple breeds.</p>

        <div class="Breed-Tags-Info">
          <div class="Breed-Tag">
            <v-icon>mdi-close</v-icon>
            <span>Turkish Angora</span>
          </div>

          <div class="Breed-Tag">
            <v-icon>mdi-close</v-icon>
            <span>British shorthair</span>
          </div>
        </div>
      </div>

      <div class="DogsBehavior wow lightSpeedIn" data-wow-delay="1s">
        <h5>How would you describe Diego’s behavior?</h5>
        <ul>
          <li>
            <input id="Friendly" type="checkbox" checked />
            <label for="Friendly">
              <div class="icon-box">
                <img src="@/assets/img/heart.svg" />
              </div>
              <p>Friendly</p>
            </label>
          </li>

          <li>
            <input id="Noisy" type="checkbox" />
            <label for="Noisy">
              <div class="icon-box">
                <img src="@/assets/img/Noisy.svg" />
              </div>
              <p>Noisy</p>
            </label>
          </li>

          <li>
            <input id="Biter" type="checkbox" />
            <label for="Biter">
              <div class="icon-box">
                <img src="@/assets/img/Biter.svg" />
              </div>
              <p>Biter</p>
            </label>
          </li>

          <li>
            <input id="Shy" type="checkbox" />
            <label for="Shy">
              <div class="icon-box">
                <img src="@/assets/img/Shy.svg" />
              </div>
              <p>Shy</p>
            </label>
          </li>

          <li>
            <input id="Fearful" type="checkbox" checked />
            <label for="Fearful">
              <div class="icon-box">
                <img src="@/assets/img/Fearful.svg" />
              </div>
              <p>Fearful</p>
            </label>
          </li>

          <li>
            <input id="Nervous" type="checkbox" />
            <label for="Nervous">
              <div class="icon-box">
                <img src="@/assets/img/Nervous.svg" />
              </div>
              <p>Nervous</p>
            </label>
          </li>
        </ul>
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