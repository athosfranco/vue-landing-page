<template>
  <v-container class="my-15">
    <v-row justify="center">
      <v-col lg="12" class="text-center">
        <v-subheader class="text-h4 justify-center">Galeria</v-subheader>
        <p>Instagram: @digitalweb</p>
      </v-col>
      <v-row class="resp">
        <v-col v-for="n in 12" :key="n" class="d-flex child-flex" cols="3">
          <v-img
            :src="`https://picsum.photos/500/300?image=${n * 2 + 10}`"
            :lazy-src="`https://picsum.photos/10/6?image=${n * 2 + 10}`"
            aspect-ratio="1"
            class="grey lighten-2"
          >
            <template v-slot:placeholder>
              <v-row class="fill-height ma-0" align="center" justify="center">
                <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
              </v-row>
            </template>
          </v-img>
        </v-col>
      </v-row>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "Gallery",
};
</script>

<style scoped>
@media (max-width: 968px) {
  .resp {
    margin: 5px;
  }
}
</style>
