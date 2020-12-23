<template>
  <v-list-item>
<img src="@/assets/uzir.png"
    width="15%" />
    <v-list-item-icon class="pa-0 mr-2">

    </v-list-item-icon>
    <v-list-item-content>
      <v-list-item-title>{{student.name}}</v-list-item-title>
      <v-list-item-subtitle>{{student.dept}}</v-list-item-subtitle>
      <v-list-item-subtitle>
      <v-btn icon :href="student.email" target="_blank">
        <v-icon>{{student.image}}</v-icon>
      </v-btn>

      </v-list-item-subtitle>

    </v-list-item-content>
  </v-list-item>
</template>

<script>
export default {
  props: {
    student: {
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