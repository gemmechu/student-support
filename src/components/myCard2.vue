<template>
 <div max-width="900">
          <v-row>

            <v-col xs8 class="col-sm-6 mx-3">
              <p
                style="color: #333;font-family: minion-pro;font-style: italic;"
              >
                <span class="mx-2" style="font-size: x-large; font-weight: 600;">" </span>
                {{story.summary}}
                 <span class="mx-2" style="font-size: x-large; font-weight: 600;">"</span>
                 <br>
                <v-card-subtitle
                  style="font-size: 16px"


                >
                  <b>{{story.name}} </b>
                  <v-btn :href="story.link" target="blank"  small class="mx-3">Read-more</v-btn>
                </v-card-subtitle>
              </p>

            </v-col>
          </v-row>
        </div>
</template>
<script>
export default {
  props: {
    story: {
      type: Object,
      default: function() {
        return {};
      }
    }
  }
};
</script>