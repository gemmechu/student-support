<template>
  <v-list-item>
    <v-list-item-content>
      <v-btn text :href="student.phone" target="_blank" class="px-0">
      <v-list-item-title  style="font-weight: 550;font-size: x-large;color: gray;">{{student.name}}</v-list-item-title>
      </v-btn>
      <v-list-item-subtitle style="color: black;font-size: smaller;font-weight: 300;">{{student.dept}}</v-list-item-subtitle>


    </v-list-item-content>
  </v-list-item>
</template>

<script>
export default {
  props: {
    about: {
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