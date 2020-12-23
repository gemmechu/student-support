<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->


    <v-img
      dark
      max-height="500px"
      src="https://cdn.vuetifyjs.com/images/backgrounds/vbanner.jpg"
    >
      <v-layout fill-height align-center>
        <v-container>
          <v-row align="center" justify="center" class="white--text">
            <v-col cols="12">
              <div
                :class="{'display-2 font-weight-bold ': $vuetify.breakpoint.smAndUp, 'title font-weight-bold': $vuetify.breakpoint.smAndDown}"
              >Welcome</div>
              <div
                :class="{'headline': $vuetify.breakpoint.smAndUp, 'subtitle-1': $vuetify.breakpoint.smAndDown}"
              >Lets Help Each other in this Time</div>
            </v-col>
          </v-row>
        </v-container>
      </v-layout>
    </v-img>
    <v-container  class="">
      <v-layout wrap>
        <v-flex xs12>
          <div class="display-1 font-weight-bold" id="mission">Our Mission</div>
        </v-flex>
        <v-flex xs12 mt-5>
          <div class="body-1">{{missionText}}</div>
          <div
            class="body-1 mt-3"
          >
          Additional
          </div>
        </v-flex>
      </v-layout>
      <v-layout wrap my-5>
        <v-flex xs12>
          <div class="display-1 font-weight-bold" id="stories">Stories</div>
        </v-flex>
        <v-flex xs12 class="mt-5">
          <br>
          <myCard/>
          <br>
          <myCard2/>
          <br>
          <myCard/>
        </v-flex>
      </v-layout>
      <v-layout wrap my-5>
        <v-flex xs12 mb-5>
          <div class="display-1 font-weight-bold" id="students"> Students</div>
        </v-flex>
        <template v-for="(student, i) in students">
          <v-flex sm6 md4 xs12 :key="i">
            <studentInfo :student="student" />
          </v-flex>
        </template>
      </v-layout>

    </v-container>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";
import studentInfo from '@/components/studentInfo.vue';
import myCard from "@/components/myCard.vue";
import myCard2 from "@/components/myCard2.vue";
export default {
  name: "home",
  components: {
    // HelloWorld,
    studentInfo,
    myCard,
    myCard2
  },
  data() {
    return {
      missionText:
        " simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic",

      students: [
        {
          name: "Bethel Haylu",
          dept: "Electrical",
          email: "mailto:uzirthapa@gmail.com",
          image: "mdi-email"
        },
        {
          name: "Bethel Haylu",
          dept: "Electrical",
          email: "mailto:uzirthapa@gmail.com",
          image: "mdi-email"
        },
        {
          name: "Bethel Haylu",
          dept: "Electrical",
          email: "mailto:uzirthapa@gmail.com",
          image: "mdi-email"
        },
        {
          name: "Bethel Haylu",
          dept: "Electrical",
          email: "mailto:uzirthapa@gmail.com",
          image: "mdi-email"
        },
        {
          name: "Bethel Haylu",
          dept: "Electrical",
          email: "mailto:uzirthapa@gmail.com",
          image: "mdi-email"
        },
        {
          name: "Bethel Haylu",
          dept: "Electrical",
          email: "mailto:uzirthapa@gmail.com",
          image: "mdi-email"
        }

      ]
    };
  }
};
</script>
