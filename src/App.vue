<template>
  <div id="app">
    <v-app id="inspire">

        <v-container style="border:1px silver solid;"  class="pa-0" >

            <v-row align="center" justify="center" style="border:1px maroon solid;" >

              <v-col class="pa-0 xs-mt-0 sm-mt-12" id="addPaddingAndMarginsHere" style="border:1px gold solid;" >

                <v-card class="elevation-12" tile style="">
                  <v-toolbar color="primary" dark flat >
                    <v-toolbar-title>
                      <FZFormHeader/>
                    </v-toolbar-title>
                  </v-toolbar>

                  <FZFormBody/>
                  <FZFormFooter/>

                </v-card>

              </v-col>
            </v-row>

        </v-container>

    </v-app>
  </div>
</template>

<script>
import FZFormHeader from './components/FZFormHeader';
import FZFormBody from './components/FZFormBody';
import FZFormFooter from './components/FZFormFooter';

export default {
  name: 'App',

  components: {
    FZFormHeader,
    FZFormBody,
    FZFormFooter
  },

  data: () => ({
    //
  }),
};
</script>
