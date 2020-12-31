<template>
  <v-list-item>
    <v-list-item-content class = "text-center">
      <v-list-item-avatar>  <img :src="require('@/assets/' + info.img + '')" /> </v-list-item-avatar>
      <v-list-item-title style="font-size: larger">{{info.name}}</v-list-item-title>
      <v-list-item-subtitle>{{info.dept}}</v-list-item-subtitle>
      <v-list-item-subtitle>{{info.school}}</v-list-item-subtitle>
      <v-list-item-subtitle>
      <v-btn icon :href="info.email" target="_blank">
        <v-icon>mdi-email</v-icon>
      </v-btn>

      <v-btn v-if="info.phone" icon :href="info.email" target="_blank">
        <v-icon>mdi-phone</v-icon>
      </v-btn>


      </v-list-item-subtitle>

    </v-list-item-content>
  </v-list-item>
</template>

<script>
export default {
  props: {
    info: {
      type: Object,
      default: function() {
        return {};
      }
    }
  }
};
</script>

<style>
</style>