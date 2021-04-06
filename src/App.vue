<template>
  <v-app>
    <v-content>
      <v-stepper v-model="e1">
        <v-stepper-header>
          <v-stepper-step
            :complete="e1 > 1"
            step="1"
          >
            Step 1
          </v-stepper-step>

          <v-divider></v-divider>
          <v-stepper-step
            :complete="e1 > 2"
            step="2"
          >
            Step 2
          </v-stepper-step >

          <v-divider></v-divider>

          <v-stepper-step step="3">
            Step 3
          </v-stepper-step>
        </v-stepper-header>

        <v-stepper-items>
          <v-stepper-content step="1">
            <v-card
              class="mb-12"
              style="color:purple"
              height="400px"
            >
            <v-img src= "./assets/Smile.png" alt="Avatar" style="width:20%"></v-img>
            <p></p>
            Hi! My name is Denis!
          </v-card>

            <v-btn
              @click="e1 = 2"
            >
              Continue
            </v-btn>

            <v-btn>
              Cancel
            </v-btn>
          </v-stepper-content>

          <v-stepper-content step="2">
            <v-card
              class="mb-12"
              style="color:purple"
              height="400px"
            >
            <img src= "./assets/MyImage.jpg" alt="Avatar" align="bottom" style="width:20%">
            <p></p>
            That's how I look like
            </v-card>

            <v-btn

              @click="e1 = 3"  >
              Continue
            </v-btn>
            <v-btn text>
              Cancel
            </v-btn>
          </v-stepper-content>

          <v-stepper-content step="3">
            <v-card
              class="mb-12"
              style="color:purple"
              height="400px"
            >
            <img src= "./assets/CatsGoSleep.jpg" alt="Avatar" align="bottom" style="width:20%">
            <p></p>
            And this is my Vuetify Stepper test!
          </v-card>

            <v-btn

              @click="e1 = 1"
            >
              Continue
            </v-btn>

            <v-btn text>
              Cancel
            </v-btn>
          </v-stepper-content>
        </v-stepper-items>
      </v-stepper>
      
    </v-content>
  </v-app>
</template>
<script>

  export default {
    data () {
      return {
        e1: 1,

        }
      },
    }
</script>

<style>
  >>>.v-btn{
    color:olive;
  }
  >>>.v-stepper{
    color:olive;
  }

</style>
