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
        style="background: white; opacity: 0.8"
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
                    Kindness is all about giving and has nothing to do with
                    getting
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
        <v-flex xs8 mt-5>
          <div class="body-1">{{ issueText }}</div>
        </v-flex>
        <v-flex>
          <!-- <iframe width="545" height="438" src="https://www.youtube.com/embed/pb7_YJp9bVA" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe> -->
        <iframe class ="my-3" width="100%" height="100%" src="https://www.youtube.com/embed/pb7_YJp9bVA" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
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
        <v-flex xs12 class="mt-2">
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
            Full Students list
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
              <v-list dense>
        <v-list-item
          v-for="(item, i) in whyDonation"
          :key="i"
        >
          <v-list-item-icon>
            <v-icon v-text="item.icon" style = "font-size:15px"></v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title style="font-size: larger;font-family: Roboto;font-weight: 400;" v-text="item.text"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>

    </v-list>

        </v-flex>
      </v-layout>
      <v-layout wrap my-5>
        <v-flex xs12>
          <div class="heading font-weight-bold" id="help">Ways to help</div>
        </v-flex>
        <v-flex xs12 mt-5>
        <v-list-item>
          <v-col cols="sm-2">
            <v-icon style = "font-size:15px">mdi-circle</v-icon>
            <span class="mx-6" style="font-size: larger;font-family: 'Roboto';font-weight: 500;">Donation</span>
          </v-col>

            <v-col class ="mr-5" cols="12" sm = "2" align-self="center"><a href=""><v-img  src="https://theme.zdassets.com/theme_assets/196447/72ab29b19ac3aa13a964e08152ed35a9e3ae95db.png"/></a> </v-col>
            <v-col cols="12" sm = "2" align-self="center"><a href=""><v-img  src="https://theme.zdassets.com/theme_assets/59547/8c140ad8c81de24e1ba81ad4f755dfde80320761.png"/></a> </v-col>

        </v-list-item>

        <v-list-item>
            <v-col cols="sm-4">
            <v-icon style = "font-size:15px">mdi-circle</v-icon>
            <span class="mx-6" style="font-size: larger;font-family: 'Roboto';font-weight: 500;">Posting on social media </span>
            </v-col>

            <v-col cols="6" sm = "2" align-self="center"><a href=""><v-img width="30%" src="https://cdn4.iconfinder.com/data/icons/social-messaging-ui-color-shapes-2-free/128/social-facebook-circle-512.png"/></a> </v-col>
            <v-col cols="6" sm = "2" align-self="center"><a href=""><v-img width="30%"  src="https://i.dlpng.com/static/png/6326845_preview.png"/></a> </v-col>
            <v-col cols="6" sm = "2" align-self="center"><a href=""><v-img width="30%"  src="https://assets.stickpng.com/thumbs/5a2fe3efcc45e43754640848.png"/></a> </v-col>

        </v-list-item>

        <v-list-item>
            <v-col cols="sm-12">
            <v-icon style = "font-size:15px">mdi-circle</v-icon>
            <span class="mx-6" style="font-size: larger;font-family: 'Roboto';font-weight: 500;">Spreading word of mouth, Email  to colleagues friends and family members</span>
            </v-col>

        </v-list-item>



        </v-flex>
      </v-layout>
      <v-layout wrap my-5>
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
      aboutText: "We are students from in AAU and from concordia trying to help students in AAU who are struggling because of current ongoing war in Tigray",
      infos:[
        {
          img: "dave.png",
          name: "Ahmed Seid",
          dept: "Business Management & Finance",
          school: "A Junior at the Concordia College in Moorhead",
          email: "mailto:ahmegoal@gmail.com",
          phone: true
          },
          {
          img: "dave.png",
          name: "Simret Araya",
          dept: "Software Engineering",
          school: "Addis Ababa University",
          email: "mailto:simretaraya7@gmail.com",
          phone: false
          },
          {
          img: "dave.png",
          name: "Gemmechu Mohammed",
          dept: "Software Engineering",
          school: "Addis Ababa University",
          email: "mailto:gemmechumohammed@gmail.com",
          phone: false
          },

      ],
      whyDonation: [
        { text: 'Give students to rent place to stay while searching a job', icon: 'mdi-circle' },
        { text: 'cover basic expenses Taxi, mobile air time, Grossaries', icon: 'mdi-circle' },
        { text: 'Allow students to be independent', icon: 'mdi-circle' },
      ],
      missionText:
        "Our mission is to alleviate the financial difficulties faced by AAU students from Tigray by mobilizing donations from generous donors like you.",
      goalText:
        "Our goal is to ensure that the students can rent a place and get other basic necessities after they graduate and leave campus so that they can search for a job and support themselves",

      issueText:
        "Currently, Ethiopia is going through a severe humanitarian crisis. Due to the ongoing conflict between the Ethiopian federal government and the Tigray regional government, a massive surge of people getting displaced to other neighboring countries and internal crisis has originated. Because of the current absence of peace and stability, Tigray students are one of the communities that are affected the most",
      whotoHelpText:
        "Prior to the Tigray crisis, Addis Ababa University’s(AAU) graduating students had been called to campus to complete their last few months of education and present their final-year thesis. The ongoing war in Tigray has affected AAU students from Tigray gravely. As is the case for many university students in Ethiopia, students rely on family for financial support. As the bank is closed and there is very limited to no means of contacting their families, these students have been struggling to continue their education and cover their cost of living. As graduation date nears, we worry what will come of the students without the help of their families and no Dorm to live in",
      stories: [
        {
          img: "dave.png",
          summary:
            "Like many of my friends, I relied on my family’s support for most of my expenses in school. Now, I am having a difficult time making ends meet. I haven’t talked to my family for about 7 weeks now. For the first time in my life I am unable to connect with my family. And not knowing what kind of situation they are in is eating me alive. The thought of quitting school and going to where they are has crossed my mind multiple times. It has been very difficult to focus on school. I want to think that things will get better but I can't help but imagine the worst case scenarios. During these hard times, my friends have been helping me with the money they get from their families. But I am worried about what will happen to me after graduation. I won't have any place to live in or any family to lean on.",
          name: "Dawit Hagos, 5th year Chemical student",
        },
        {
          img: "destawit.png",
          summary:
            "When our school closed because of the pandemic we were forced to pause our education and go home. My father had passed away a few months before that so I took a job to financially support my family. With my new job I was able to support my mother and two sisters, and even save some money in the bank. Now I can’t go to my family and they can’t come to me. And because my account was frozen because my bank is in tigray, I find myself tagging along with my friends and asking for their help to even get things as important as a sanitary pad. I can’t attend my graduation, what should have been the happiest day after 5 years of hard work, because I don’t have money to cover my graduation costs.",
          name: "Destawit fiseha, 5th year Chemical student",
        },
        {
          img: "efrem.png",
          summary:
            "I haven’t been able to contact my family because phones don’t work where they are. I worry about them day and night. My brother was able to cross to Sudan and call me from there. He told me that he had no money and asked for my help. I told him I had nothing to give him, and that he should go to the refugee camp and try to get help there. I felt helpless, not being able to help my own brother was one of the most dreadful moments in my life. I can't focus on my school work because I worry about my family and what I will do after graduation. I don’t even have money to buy a mattress to sleep on and that has been stressful.",
          name: "Efriem Tsegay, 5th year Chemical student",
        },
      ],
      students: [
        {
          name: "Efrem Tsegay",
          dept: "5th year, Chemical student",
          phone: "tel:+25125328096",
        },
        {
          name: "Daniel Haglush",
          dept: "5th year, Chemical student",
          phone: "tel:+25125328096",
        },
        {
          name: "Dawit Hagos",
          dept: "5th year, Chemical student",
          phone: "tel:+25125328096",
        },
        {
          name: "Daniel G/mariam",
          dept: "5th year, Chemical student",
          phone: "tel:+25125328096",
        },
        {
          name: "Yared Luel",
          dept: "5th year, Chemical student",
          phone: "tel:+25125328096",
        },
        {
          name: "Ashenafi",
          dept: "5th year, Chemical student",
          phone: "tel:+25125328096",
        },
        {
          name: "Biniyam Aregawi",
          dept: "5th year, Chemical student",
          phone: "tel:+25125328096",
        },
        {
          name: "Dawti Fiseha",
          dept: "5th year, Chemical student",
          phone: "tel:+25125328096",
        },
        {
          name: "Birtukan",
          dept: "5th year, Chemical student",
          phone: "tel:+25125328096",
        },
        {
          name: "Nathinal Kahsay",
          dept: "5th year, Chemical student",
          phone: "tel:+25125328096",
        },
        {
          name: "Awaha Guash",
          dept: "5th year, Chemical student",
          phone: "tel:+25125328096",
        },
        {
          name: "Muez Kalayu",
          dept: "5th year, Chemical student",
          phone: "tel:+25125328096",
        },
        {
          name: "Tana",
          dept: "5th year, Chemical student",
          phone: "tel:+25125328096",
        },
        {
          name: "Ataklti",
          dept: "5th year, Chemical student",
          phone: "tel:+25125328096",
        },
        {
          name: "Solomon",
          dept: "5th year, Chemical student",
          phone: "tel:+25125328096",
        },
        {
          name: "Goytom Giday",
          dept: "5th year, Chemical student",
          phone: "tel:+25125328096",
        },
      ],
    };
  },
};
</script>
