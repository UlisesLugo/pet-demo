<script>
export default {
  name: "NavBar",
  components: {},
};
</script>

<template>
  <v-navigation-drawer>
    <v-list>
      <v-list-item title="El mundo de las mascotas"></v-list-item>
    </v-list>

    <v-list nav>
      <v-list-item title="Gatos"></v-list-item>
      <v-list-item title="Perros"></v-list-item>
      <v-list-item title="Serpientes"></v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>

<style>
</style>