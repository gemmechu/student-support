<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->

    <v-img
      max-height="500px"
      src="https://opportunitydesk.org/wp-content/uploads/2016/04/African-Students.jpg"
    >
      <v-layout
        fill-height
        align-center
        style="background: white; opacity: 0.77"
      >
        <v-container>
          <v-row align="center" justify="center" class="white--text">
            <v-col cols="12">
              <div style="position: relative">
                <br />
                <br />
                <div class="text-center text-uppercase" id="mission">
                  <h1
                    style="
                      font-size: xxx-large;
                      font-family: DINBlack;
                      color: #000;
                      line-height: 1.2;
                    "
                  >
                    Let’s support our fellow students
                    <br />
                    in need of our help
                  </h1>
                  <h2 class="qoute" style="">
                    Kindness is Giving hope to those who think they are all alone in this world
                    <span style="color: black;font-size: smaller;"> - paktivist</span>
                  </h2>

                </div>
              </div>
            </v-col>
          </v-row>
        </v-container>
      </v-layout>
    </v-img>
    <v-container class="my-5">
      <v-layout wrap my-5>
        <v-flex xs12>
          <div class="heading font-weight-bold" id="mission">Our Mission</div>
        </v-flex>
        <v-flex xs12 mt-5>
          <div class="body-1">{{ missionText }}</div>
        </v-flex>
      </v-layout>
      <v-layout wrap my-5>
        <v-flex xs12>
          <div class="heading font-weight-bold" id="goal">Our Goal</div>
        </v-flex>
        <v-flex xs12 mt-5>
          <div class="body-1">{{ goalText }}</div>
        </v-flex>
      </v-layout>
      <v-layout wrap my-5>
        <v-flex xs12>
          <div class="heading font-weight-bold" id="issue">
            What is the Issue
          </div>
        </v-flex>
        <v-flex xs12 sm6 mt-5>
          <div class="body-1">{{ issueText }}</div>
        </v-flex>
        <v-flex sm4>

        <iframe class ="my-3" width="100%" height="100%" src="https://www.youtube.com/embed/KHO0sVKgOsY" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
        </v-flex>
      </v-layout>

      <v-layout wrap my-5>
        <v-flex xs12>
          <div class="heading font-weight-bold" id="students">
            Who do we help
          </div>
        </v-flex>
        <v-flex xs12 mt-5>
          <div class="body-1">{{ whotoHelpText }}</div>
        </v-flex>
        <v-flex xs12 class="mt-2 mx-8">
          <br />
          <br />
          <myCard :story="stories[1]" />
          <br />
          <br />
          <myCard2 :story="stories[0]" />
          <br />
          <br />
          <myCard :story="stories[2]" />
          <br />
          <br />
        </v-flex>
      </v-layout>
      <v-layout wrap my-5>
        <v-flex xs12 mb-5>
          <div class="heading text-center" id="">
            Students list
          </div>
        </v-flex>
        <template v-for="(student, i) in students">
          <v-flex sm4 md3 xs6 :key="i">
            <studentInfo :student="student" />
          </v-flex>
        </template>
      </v-layout>
      <v-layout wrap my-5>
        <v-flex xs12>
          <div class="heading font-weight-bold" id="impact">
            How does your donation make an Impact
          </div>
        </v-flex>
        <v-flex xs12 mt-5 mx-8>
              <v-list>
        <v-list-item

          v-for="(item, i) in whyDonation"
          :key="i"

        >
          <v-list-item-icon>
            <v-icon v-text="item.icon" style = "font-size:1em"></v-icon>
          </v-list-item-icon>

          <v-list-item-title  style="font-size: larger;font-family: Roboto;font-weight: 400;" v-text="item.text"></v-list-item-title>

        </v-list-item>

    </v-list>

        </v-flex>
      </v-layout>
      <v-layout wrap my-5>
        <v-flex xs12>
          <div class="heading font-weight-bold" id="help">Ways to help</div>
        </v-flex>
        <v-flex xs12 mt-5>

          <v-row>
            <v-col cols="sm-2">
            <v-icon style = "font-size:15px">mdi-circle</v-icon>
            <span class="mx-6" style="font-size: larger;font-family: 'Roboto';font-weight: 500;">Donate: </span>
          </v-col>
          </v-row>
          <v-row class="mx-5">
          <v-col cols="2" sm = "2" align-self="center"><a target="_blank" href="https://www.gofundme.com/f/help-students-have-hope-again?utm_source=customer&utm_medium=copy_link&utm_campaign=p_cf+share-flow-1"><v-img  src="https://theme.zdassets.com/theme_assets/196447/72ab29b19ac3aa13a964e08152ed35a9e3ae95db.png"/></a> </v-col>
          </v-row>





        <v-row>
          <v-col cols="sm-4">
            <v-icon style = "font-size:15px">mdi-circle</v-icon>
            <span class="mx-6" style="font-size: larger;font-family: 'Roboto';font-weight: 500;">Share it on: `</span>
            </v-col>
        </v-row>
        <v-row class="mx-5">
          <v-col cols="2" sm = "2" align-self="center"><a href="https://www.facebook.com/helpstudents.aautigray.9/about" target="_blank"><v-img width="30%" src="@/assets/fb.png"/></a> </v-col>
            <v-col cols="2" sm = "2" align-self="center"><a href="https://www.instagram.com/aau_student_aid/" target="_blank"><v-img width="30%"  src="@/assets/insta.png"/></a> </v-col>
            <v-col cols="2" sm = "2" align-self="center"><a href=""><v-img width="30%"  src="@/assets/twitter.png"/></a> </v-col>
        </v-row>


        </v-flex>
      </v-layout>
      <v-layout wrap my-5 >
        <v-flex xs12>
          <div class="heading font-weight-bold" id="aboutUs">About Us</div>
        </v-flex>
        <v-flex xs12 mt-5>
          <div class="body-1">{{ aboutText }}</div>
        </v-flex>
         <template v-for="(info, i) in infos">
          <v-flex sm4 md4 xs6 :key="i">
            <aboutUs :info="info" />
          </v-flex>
        </template>

      </v-layout>
    </v-container>
  </div>
</template>
<style>
.body-1 {
  width: 85%;
}
.heading {
  text-transform: uppercase;
  font-size: xx-large;
  font-family: "Roboto";
  color: #333;
}
.qoute {
  color: #9b242d;
  text-transform: initial;
  font-family: "minion-pro";
  font-style: italic;
  font-weight: 500;
  line-height: 1;
}
</style>
<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";
import studentInfo from "@/components/studentInfo.vue";
import myCard from "@/components/myCard.vue";
import myCard2 from "@/components/myCard2.vue";
import aboutUs from '@/components/aboutUs.vue';
export default {
  name: "home",
  components: {
    // HelloWorld,
    studentInfo,
    myCard,
    myCard2,
    aboutUs
  },
  data() {
    return {
      aboutText: "We are students from  Addis Ababa University and Concordia college trying to help graduating students in AAU who are currently struggling because of the ongoing war in Tigray.",
      infos:[
        {
          img: "ahmed.jpg",
          name: "Ahmed Seid",
          dept: "Business Management & Finance",
          school: "Concordia College",
          email: "mailto:ahmegoal@gmail.com",
          phone: true,
          number: "tel:+14049339682"
          },
          {
          img: "simret.jpg",
          name: "Simret Araya",
          dept: "Software Engineering",
          school: "Addis Ababa University",
          email: "mailto:simretaraya7@gmail.com",
          phone: false
          },
          {
          img: "gemme.jpg",
          name: "Gemmechu Mohammed",
          dept: "Software Engineering",
          school: "Addis Ababa University",
          email: "mailto:gemmechumohammed@gmail.com",
          phone: false
          },

      ],
      whyDonation: [
        { text: 'Gives students the financial help to get a place to stay while searching for a Job', icon: 'mdi-circle' },
        { text: 'Covers basic expenses such as: transportation, mobile air time, groceries etc', icon: 'mdi-circle' },
        { text: 'helps students to be independent until it is safe to return to their families', icon: 'mdi-circle' },
      ],
      missionText:
        "Our mission is to alleviate the financial difficulties faced by AAU students from Tigray by mobilizing donations from generous donors like you.",
      goalText:
        "Our goal is to ensure that the students can rent a place and get other basic necessities after they graduate and leave campus so that they can search for a job and support themselves",

      issueText:
        "Currently, Ethiopia is going through a severe humanitarian crisis. Due to the ongoing war between the Ethiopian federal government and the Tigray regional government, a massive surge of people getting displaced to other neighboring countries and internal crisis has originated. Because of the current absence of peace and stability, Tigray students are one of the communities that are getting affected the most",
      whotoHelpText:
        "Prior to the current crisis, Addis Ababa University’s(AAU) graduating students had been called to campus to complete their last few months of education and present their final-year thesis. Unfortunately, the ongoing war in Tigray has affected AAU students from Tigray gravely. Similar to many university students in Ethiopia, Tigray students rely on family for their financial support. As the bank is closed and there is very limited to no means of contacting their families, these students have been struggling to continue their education and cover their cost of living. As graduation date nears, we worry what will come of the students without the help of their families and no Dorm to live in",
      stories: [
        {
          link:"https://docs.google.com/document/d/1MnVZBhc3VfEl6j1BEmZeDoE5ZiCRlEyIpa0H8SkC-Zs/edit?usp=sharing",
          img: "dave.png",
          summary:
            "Like many of my friends, I relied on my family’s support for most of my expenses in school. Now, I am having a difficult time making ends meet. I haven’t talked to my family for about 7 weeks now. For the first time in my life I am unable to connect with my family. And, the constant worry of not knowing the situation they are in is eating me alive.",
          name: "Dawit Hagos, 5th year AAiT Student",
        },
        {
          img: "destawit.png",
          link:"https://docs.google.com/document/d/1BnfRwXxfU_PmjkI7gy7RHtrgGuCKP-hJJEA7D-_ihVQ/edit?usp=sharing",
          summary:
            "I believe the current situation has not just been financially, but psychologically daunting to me. There is no support system placed in the university. No one is asking us how we’re doing or what we’re dealing with. It is so sad to feel so alone in the world yet surrounded by so many people.",
          name: "Destawit fiseha, 5th year AAiT Student",
        },
        {
          img: "efrem.png",
          link:"https://docs.google.com/document/d/1hViA0IPfrFSCHm_pXjxGvXqQY4PC-VOTHW92ethuX4s/edit?usp=sharing",
          summary:
            "The fact that my future becomes uncertain after I graduate is truly concerning to me  as I am required to leave the campus and I have nowhere to stay too. Recently, i also got a call from my little brother as he shared a shocking news to me that he crossed a border to Sudan with no money or any sort of support. Hearing that news has been one of the most dreadful moments in my life, and I can only wish that I could get some stability until the war is over so that I can get a job and help out my brother and families.",
          name: "Efriem Tsegay, 5th year AAiT Student",
        },
      ],
      students: [
        {
          name: "Efrem Tsegay",
          dept: "5th year, AAiT Student",
          phone: "tel:+25125328096",
        },
        {
          name: "Daniel Haglush",
          dept: "5th year, AAiT Student",
          phone: "tel:+25125328096",
        },
        {
          name: "Dawit Hagos",
          dept: "5th year, AAiT Student",
          phone: "tel:+25125328096",
        },
        {
          name: "Daniel G/mariam",
          dept: "5th year, AAiT Student",
          phone: "tel:+25125328096",
        },
        {
          name: "Yared Luel",
          dept: "5th year, AAiT Student",
          phone: "tel:+25125328096",
        },
        {
          name: "Ashenafi",
          dept: "5th year, AAiT Student",
          phone: "tel:+25125328096",
        },
        {
          name: "Biniyam Aregawi",
          dept: "5th year, AAiT Student",
          phone: "tel:+25125328096",
        },
        {
          name: "Dawti Fiseha",
          dept: "5th year, AAiT Student",
          phone: "tel:+25125328096",
        },
        {
          name: "Birtukan",
          dept: "5th year, AAiT Student",
          phone: "tel:+25125328096",
        },
        {
          name: "Nathinal Kahsay",
          dept: "5th year, AAiT Student",
          phone: "tel:+25125328096",
        },
        {
          name: "Awaha Guash",
          dept: "5th year, AAiT Student",
          phone: "tel:+25125328096",
        },
        {
          name: "Muez Kalayu",
          dept: "5th year, AAiT Student",
          phone: "tel:+25125328096",
        },
        {
          name: "Tana",
          dept: "5th year, AAiT Student",
          phone: "tel:+25125328096",
        },
        {
          name: "Ataklti",
          dept: "5th year, AAiT Student",
          phone: "tel:+25125328096",
        },
        {
          name: "Solomon",
          dept: "5th year, AAiT Student",
          phone: "tel:+25125328096",
        },
        {
          name: "Goytom Giday",
          dept: "5th year, AAiT Student",
          phone: "tel:+25125328096",
        },
      ],
    };
  },
};
</script>
