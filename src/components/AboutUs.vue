<template>
  <v-container>
    <div class="container">
      <v-col lg="6">
        <img src="../assets/progress.svg" alt="" width="100%" />
      </v-col>

      <v-col lg="6">
        <v-subheader class="text-h4">Sobre Nós</v-subheader>
        <p class="pl-4">
          Somos uma agência que atua a mais de 10 anos no mercado de desenvolvimento de produtos digitais e já ajudamos
          centenas de clientes a transformarem e elevarem seus produtos ao topo. A nossa equipe é composta pelos
          melhores UI/UX designers, desenvolvedores e publicitários do mercado.
        </p>

        <v-list-item>
          <v-icon class="pr-3" color="success">mdi-check-all</v-icon>
          <v-list-item-subtitle> 800+ projetos finalizados</v-list-item-subtitle>
        </v-list-item>
        <v-list-item>
          <v-icon class="pr-3" color="success">mdi-check-all</v-icon>
          <v-list-item-subtitle> 300+ empresas satisfeitas</v-list-item-subtitle>
        </v-list-item>
        <v-list-item>
          <v-icon class="pr-3" color="success">mdi-check-all</v-icon>
          <v-list-item-subtitle>150+ desenvolvedores talentosos </v-list-item-subtitle>
        </v-list-item>
      </v-col>
    </div>
  </v-container>
</template>

<script>
export default {
  name: "AboutUs",
};
</script>

<style scoped>
.container {
  display: flex;
}
@media (max-width: 968px) {
  .container {
    flex-direction: column;
  }
}
</style>
