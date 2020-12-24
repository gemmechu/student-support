<template>
 <div
          max-width="900"


        >
          <v-row>
            <img
                class="mx-3"
                src="@/assets/uzir.png"
                width="26%"
            />
            <v-col class="mx-5">
              <p
                style="line-height: 26px;
                font-size: 15px;
                font-style: italic;
                width: 48em;"
              >
                <span class="mx-3" style="font-size: x-large; font-weight: 600;">" </span>
                  {{story.summary}}
                 <span class="mx-2" style="font-size: x-large; font-weight: 600;">"</span>
                  <br>

                <v-card-subtitle
                  style="font-size: 16px"
                >
                  <b> {{story.name}} </b>
                  <v-btn small class="mx-3">Read-more</v-btn>
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
