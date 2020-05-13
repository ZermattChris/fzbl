<template>
  <div id="app">
    <v-app id="inspire"><v-app id="inspire">

        <v-container style="border:1px silver solid;" 
            class="fill-height"
            fluid
          >
            <v-row align="center" justify="center" style="border:1px maroon solid;" >
              <v-col cols="12" sm="8" md="4" style="border:1px gold solid;">

                <v-card class="elevation-12" tile>
                  <v-toolbar color="primary" dark flat >
                    <v-toolbar-title>
                      <FZFormHeader/>
                    </v-toolbar-title>
                  </v-toolbar>

                  <FZFormBody/>
                  <!-- <FZFormFooter/> -->

                </v-card>

              </v-col>
            </v-row>

        </v-container>

    </v-app></v-app>
  </div>
</template>

<script>
import FZFormHeader from './components/FZFormHeader';
import FZFormBody from './components/FZFormBody';
// import FZFormFooter from './components/FZFormFooter';

export default {
  name: 'App',

  components: {
    FZFormHeader,
    FZFormBody
  },

  data: () => ({
    //
  }),
};
</script>
