<template>
  <v-card
    class="mx-auto fill-height "
    max-width="900"
    fluid
  >
    <v-card-title class="title font-weight-regular justify-space-between">
      <span>{{ currentTitle }}</span>
      <v-avatar
        color="primary lighten-2"
        class="subheading white--text"
        size="24"
        v-text="step"
      ></v-avatar>
    </v-card-title>

    <v-window v-model="step">
      <v-window-item :value="1">
        <v-card-text >
          <v-text-field
            label="Email"
            value="info@flyzermatt.com"
          ></v-text-field>
          <span class="caption grey--text text--darken-1">
            This is the email you will use to login to your Vuetify account
          </span>
        </v-card-text>
      </v-window-item>

      <v-window-item :value="2">
        <v-card-text>
          <v-text-field
            label="Password"
            type="password"
          ></v-text-field>
          <v-text-field
            label="Confirm Password"
            type="password"
          ></v-text-field>
          <span class="caption grey--text text--darken-1">
            Please enter a password for your account
          </span>
        </v-card-text>
      </v-window-item>

      <v-window-item :value="3">
        <div class="pa-4 text-center">
          <v-img
            class="mb-4"
            contain
            height="128"
            src="@/assets/flyzermatt-logo-box-shadow.svg"
          ></v-img>
          <h3 class="title font-weight-light mb-2" style="letter-spacing:0.3em !important;">PARAGLIDING</h3>
          <span class="caption grey--text">Thanks for Booking! (You'll hear from us shortly)</span>
        </div>
      </v-window-item>
    </v-window>

    <v-footer
      absolute
      style="padding-bottom:20px; background-color:white;"
    >
      <v-btn
        :disabled="step === 1"
        text
        @click="step--"
      > Back </v-btn>
      <v-spacer></v-spacer>
      <v-btn
        :disabled="step === 3"
        color="primary"
        depressed
        @click="step++"
      > Next </v-btn>
    </v-footer>

  </v-card>
</template>

<script>
  export default {
    data: () => ({
      step: 1,
    }),

    computed: {
      currentTitle () {
        switch (this.step) {
          case 1: return 'Get started'
          case 2: return 'Choose a Time to fly'
          default: return 'Booking sent'
        }
      },
    },
  }
</script>