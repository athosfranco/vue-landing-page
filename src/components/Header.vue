<template>
  <v-app-bar app color="white" light elevation="6">
    <v-toolbar-title><v-icon class="icon">mdi-fingerprint</v-icon>DW</v-toolbar-title>
    <v-spacer />
    <v-list class="d-flex align-center justify-around">
      <v-list-item link v-for="(menu, index) in menus" :key="index" :to="menu.route">
        <v-list-item-title>{{ menu.title }}</v-list-item-title>
      </v-list-item>
      <v-btn text>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
      <v-btn outlined color="success">Login</v-btn>
    </v-list>
  </v-app-bar>
</template>

<script>
export default {
  name: "Header",
  data: () => ({
    menus: [
      { title: "Início", route: "home" },
      { title: "Sobre Nós", route: "about-us" },
      { title: "Projetos", route: "projects" },
      { title: "Galeria", route: "gallery" },
      { title: "Contato", route: "contato" },
    ],
  }),
};
</script>

<style></style>
