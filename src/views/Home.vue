<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->


    <v-img
      style="opacity: 0.5;"
      max-height="500px"
      src="https://opportunitydesk.org/wp-content/uploads/2016/04/African-Students.jpg"
    >
      <v-layout fill-height align-center>
        <v-container>
          <v-row align="center" justify="center" class="white--text">
            <v-col cols="12">
              <div style="position: relative;"
              >
              <br>
              <br>
              <div class="display-1 font-weight-bold text-center text-uppercase" id="mission">
                <p style="font-size: xxx-large; color: #000; opacity:1;">Let’s support our fellow students </p>
                <p style="font-size: xxx-large; color: #000;  opacity:1 !important;">  in need of our help </p></div>
              </div>
            </v-col>
          </v-row>
        </v-container>
      </v-layout>
    </v-img>
    <v-container  class="my-5">
      <v-layout wrap my-5>
        <v-flex xs12>
          <div class="display-1 font-weight-bold" id="mission">Our Mission</div>
        </v-flex>
        <v-flex xs12 mt-5>
          <div class="body-1">{{missionText}}</div>
         </v-flex>
      </v-layout>
            <v-layout wrap my-5>
        <v-flex xs12>
          <div class="display-1 font-weight-bold" id="mission">What is the Issue?</div>
        </v-flex>
        <v-flex xs12 mt-5>
          <div class="body-1">{{issueText}}</div>

        </v-flex>
      </v-layout>

      <v-layout wrap my-5>
        <v-flex xs12>
          <div class="display-1 font-weight-bold" id="stories">Who do we help?</div>
        </v-flex>
        <v-flex xs12 class="mt-2">
          <br>
          <br>
          <myCard :story="stories[0]" />
          <br>
          <br>
          <myCard2 :story="stories[1]"/>
          <br>
          <br>
          <myCard :story="stories[2]"/>
          <br>
          <br>
          <br>
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
      issueText:'Currently, Ethiopia is going through a severe humanitarian crisis. Due to the ongoing conflict between the Ethiopian federal government and the Tigray regional government, a massive surge of people getting displaced to other neighboring countries and internal crisis has originated. Because of the current absence of peace and stability, Tigray students are one of the communities that are affected the most.',
      missionText:
        "Our mission is to alleviate the financial difficulties faced by AAU students from Tigray by mobilizing donations from generous donors like you.",

      stories: [
        {
         img: "",
         summary: "Like many of my friends, I relied on my family’s support for most of my expenses in school. Now, I am having a difficult time making ends meet. I haven’t talked to my family for about 7 weeks now. For the first time in my life I am unable to connect with my family. And not knowing what kind of situation they are in is eating me alive. The thought of quitting school and going to where they are has crossed my mind multiple times. It has been very difficult to focus on school. I want to think that things will get better but I can't help but imagine the worst case scenarios. During these hard times, my friends have been helping me with the money they get from their families. But I am worried about what will happen to me after graduation. I won't have any place to live in or any family to lean on.",
         name:"Dawit Hagos, 5th year Chemical student",

        },
        {
         img: "",
         summary: "When our school closed because of the pandemic we were forced to pause our education and go home. My father had passed away a few months before that so I took a job to financially support my family. With my new job I was able to support my mother and two sisters, and even save some money in the bank. Now I can’t go to my family and they can’t come to me. And because my account was frozen because my bank is in tigray, I find myself tagging along with my friends and asking for their help to even get things as important as a sanitary pad. I can’t attend my graduation, what should have been the happiest day after 5 years of hard work, because I don’t have money to cover my graduation costs.",
         name:"Destawit fiseha, 5th year Mechanical student",

        },
        {
         img: "",
         summary: "I haven’t been able to contact my family because phones don’t work where they are. I worry about them day and night. My brother was able to cross to Sudan and call me from there. He told me that he had no money and asked for my help. I told him I had nothing to give him, and that he should go to the refugee camp and try to get help there. I felt helpless, not being able to help my own brother was one of the most dreadful moments in my life. I can't focus on my school work because I worry about my family and what I will do after graduation. I don’t even have money to buy a mattress to sleep on and that has been stressful.",
         name:"Efriem Tsegay, 5th year Electrical student",

        }

      ],
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
