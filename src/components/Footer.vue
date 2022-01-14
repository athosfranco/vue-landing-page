<template>
  <v-footer dark padless>
    <v-card class="flex" flat tile>
      <v-card-title style="background-color: #5ab55e; height: 100px" class="resp">
        <v-btn v-for="icon in icons" :key="icon" class="mx-4" dark icon>
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-title>

      <v-card-text class="py-2 white--text text-center">
        {{ new Date().getFullYear() }} —
        <strong
          >Digital Web - Made with 💚 by <a href="https://github.com/athosfranco" target="_blank">Athos Franco</a>
        </strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  name: "Footer",
  data: () => ({
    icons: ["mdi-github", "mdi-linkedin", "mdi-twitter"],
  }),
};
</script>

<style scoped>
.resp {
  display: flex;
  justify-content: center;
}
</style>
