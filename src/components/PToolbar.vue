<template>
  <v-app-bar fixed flat dark style="background-color: #000; " >
    <v-layout justify-center>
      <v-container>
        <v-layout>
          <div style="font-style: italic;font-family: serif !important;font-size: 1.625rem !important;"
            :class="{'display-1 font-weight-bold': $vuetify.breakpoint.smAndUp,'title font-weight-bold': $vuetify.breakpoint.smAndDown, }"
          >Help Students</div>
          <v-spacer></v-spacer>
          <v-toolbar-items class="text-right">
            <v-btn
              :x-small="$vuetify.breakpoint.smAndDown"
              @click="$vuetify.goTo('#mission',options )"
              text
            >Mission</v-btn>
            <v-btn
              :x-small="$vuetify.breakpoint.smAndDown"
              @click="$vuetify.goTo('#goal',options )"
              text
            >Goal</v-btn>
             <v-btn
              :x-small="$vuetify.breakpoint.smAndDown"
              @click="$vuetify.goTo('#issue',options )"
              text
            >Issue</v-btn>
            <v-btn
              :x-small="$vuetify.breakpoint.smAndDown"
              @click="$vuetify.goTo('#students',options )"
              text
            >Students</v-btn>
             <v-btn
              :x-small="$vuetify.breakpoint.smAndDown"
              @click="$vuetify.goTo('#impact',options )"

            >impact</v-btn>
            <v-btn
              :x-small="$vuetify.breakpoint.smAndDown"
              @click="$vuetify.goTo('#help',options )"

            >ways to help</v-btn>
            <v-btn
              :x-small="$vuetify.breakpoint.smAndDown"
              @click="$vuetify.goTo('#aboutUs',options )"

            >About Us</v-btn>


          </v-toolbar-items>
        </v-layout>
      </v-container>
    </v-layout>
  </v-app-bar>
</template>

<script>
// import * as easings from "vuetify/es5/services/goto/easing-patterns";
export default {
  data() {
    return {
      options: {
        duration: 300,
        offset: 0,
        easing: "easeInOutCubic"
      }
    };
  }
};
</script>

<style>
</style>