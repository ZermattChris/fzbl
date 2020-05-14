<template>
  <div id="app">
    <v-app>

      <v-row class="py-md-12" justify="center" style="background-color:silver;">
        <v-col class="pa-0 " 
          md="7"
          style=""
        >

          <v-card class="fill-height" style="box-shadow:none;" tile fluid>
            <!-- <v-toolbar color="primary" dark flat >
              <v-toolbar-title>
                <FZFormHeader/>
              </v-toolbar-title>
            </v-toolbar> -->

            <FZFormBody/>
            <FZFormFooter/>

          </v-card>

        </v-col>
      </v-row>

    </v-app>
  </div>
</template>

<script>
// import FZFormHeader from './components/FZFormHeader';
import FZFormBody from './components/FZFormBody';
import FZFormFooter from './components/FZFormFooter';

export default {
  name: 'App',

  components: {
    FZFormBody,
    FZFormFooter
  },

  data: () => ({
    //
  }),
};
</script>
