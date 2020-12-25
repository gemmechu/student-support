<template>
 <div
          max-width="900"


        >
          <v-row>

            <v-col class="ml-10"  style="flex-grow: 0;">
              <p
                style="color: #333;font-family: minion-pro;font-style: italic;width: 45em;"
              >
                <span class="mx-3" style="font-size: x-large; font-weight: 600;">" </span>
                {{story.summary}}
                 <span class="mx-2" style="font-size: x-large; font-weight: 600;">"</span>
                 <br>
                <v-card-subtitle
                  style="font-size: 16px"


                >
                  <b>{{story.name}} </b>
                  <v-btn small class="mx-3">Read-more</v-btn>
                </v-card-subtitle>
              </p>

            </v-col>
             <img
                class="mx-3"
                :src="require('@/assets/' + story.img + '')"
                width="26%"
            />
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