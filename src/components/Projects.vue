<!--- ESTRUTURA ----->
<template>
  <v-container class="my-15">
    <v-row class="responsiveness" justify="center">
      <v-col lg="12" class="text-center">
        <v-subheader class="text-h4 justify-center">Projetos</v-subheader>
        <p>Dê uma olhada nos nossos trabalhos anteriores.</p>
      </v-col>
      <v-col lg="12">
        <div class="text-center">
          <!--- "TAGS" QUE CONTROLAM QUAL TIPO DE PROJETO ESTÁ SENDO EXIBIDO ----->
          <v-chip @click="activeTab = 'uiux'" :color="activeTab === 'uiux' ? 'success' : ''" class="mx-5">UI/UX</v-chip>
          <v-chip @click="activeTab = 'web'" :color="activeTab === 'web' ? 'success' : ''" class="mx-5 my-1"
            >Web Apps</v-chip
          >
          <v-chip @click="activeTab = 'mobile'" :color="activeTab === 'mobile' ? 'success' : ''" class="mx-5 my-1"
            >Mobile Apps</v-chip
          >
          <v-chip @click="activeTab = 'publi'" :color="activeTab === 'publi' ? 'success' : ''" class="mx-5 my-1"
            >Publicidade</v-chip
          >
        </div>
      </v-col>
      <!--- EXIBIÇÃO DO GRID COM OS PROJETOS ----->
      <!--- ---------------------------------------------------------------------------------------------  ----->
      <slot v-if="activeTab === 'web'">
        <!--- projetos web ----->
        <v-col lg="3" v-for="(web, webindex) in webApps" :key="webindex">
          <v-card>
            <v-img
              :src="web.image"
              class="white--text align-end"
              gradient="to bottom, rgba(0,0,0,0.1), rgba(0,0,0,0.5)"
              height="200px"
            ></v-img>
            <v-card-title>{{ web.title }} #{{ webindex + 1 }} </v-card-title>
          </v-card>
        </v-col>
      </slot>
      <!--- ---------------------------------------------------------------------------------------------  ----->
      <slot v-if="activeTab === 'uiux'">
        <!--- projetos ui/ux design ----->
        <v-col lg="3" v-for="(design, designindex) in designs" :key="designindex">
          <v-card>
            <v-img
              :src="design.image"
              class="white--text align-end"
              gradient="to bottom, rgba(0,0,0,0.1), rgba(0,0,0,0.5)"
              height="200px"
            ></v-img>
            <v-card-title>{{ design.title }} #{{ designindex + 1 }}</v-card-title>
          </v-card>
        </v-col>
      </slot>
      <!--- ---------------------------------------------------------------------------------------------  ----->
      <slot v-if="activeTab === 'mobile'">
        <!--- projetos mobile ----->
        <v-col lg="3" v-for="(mobile, mobileIndex) in mobile" :key="mobileIndex">
          <v-card shaped>
            <v-img
              :src="mobile.image"
              class="white--text align-end"
              gradient="to bottom, rgba(0,0,0,0.1), rgba(0,0,0,0.5)"
              height="200px"
            ></v-img>
            <v-card-title>{{ mobile.title }} #{{ mobileIndex + 1 }}</v-card-title>
          </v-card>
        </v-col>
      </slot>
      <!--- ---------------------------------------------------------------------------------------------  ----->
      <slot v-if="activeTab === 'publi'">
        <!--- projetos publi ----->
        <v-col lg="3" v-for="(publi, publiIndex) in publi" :key="publiIndex">
          <v-card>
            <v-img
              :src="publi.image"
              class="white--text align-end"
              gradient="to bottom, rgba(0,0,0,0.1), rgba(0,0,0,0.5)"
              height="200px"
            ></v-img>
            <v-card-title>{{ publi.title }} #{{ publiIndex + 1 }}</v-card-title>
          </v-card>
        </v-col>
      </slot>
      <!--- ---------------------------------------------------------------------------------------------  ----->
    </v-row>
  </v-container>
</template>

<!--- logica ----->
<script>
export default {
  name: "Projects",
  data: () => ({
    activeTab: "web",
    webApps: [
      {
        title: "Webapp",
        image:
          "https://cdn.dribbble.com/users/1150809/screenshots/17270646/media/5c93c4cbc299e9dbb36862cb41753d7e.jpg?compress=1&resize=1200x900&vertical=top",
      },
      {
        title: "Webapp",
        image: "https://agiletech.vn/wp-content/uploads/2020/11/5b9eb02872831d29ba6e4d5ea0074a27.jpg",
      },
      {
        title: "Webapp",
        image:
          "https://cdn.dribbble.com/users/1904192/screenshots/17272173/media/eefcee09e975e3f98ca1c148c7cfb852.png?compress=1&resize=1200x900&vertical=top",
      },
      {
        title: "Webapp",
        image:
          "https://cdn.dribbble.com/users/1998175/screenshots/17252579/media/7696e05bbbe3f7515c7d25b0ab8931fd.png?compress=1&resize=1200x900&vertical=top",
      },
      {
        title: "Webapp",
        image:
          "https://cdn.dribbble.com/users/6047818/screenshots/15695514/media/fec8c9d6a86c3d8124dd2031f6673756.png?compress=1&resize=1200x900&vertical=top",
      },
      {
        title: "Webapp",
        image:
          "https://cdn.dribbble.com/users/774375/screenshots/16211602/media/9ef8bbae05dba670e1c57c44aa7223f4.png?compress=1&resize=1200x900&vertical=top",
      },
    ],
    designs: [
      {
        title: "Design",
        image:
          "https://cdn.dribbble.com/users/1254731/screenshots/16322776/media/f5b91a7b51db002dd24afb587e3d275d.jpg?compress=1&resize=1200x900&vertical=top",
      },
      {
        title: "Design",
        image:
          "https://cdn.dribbble.com/users/2504/screenshots/16969134/media/c323f1f5689dce0e8c35f46cc4bdcc56.jpg?compress=1&resize=1200x900&vertical=top",
      },
      {
        title: "Design",
        image: "https://agiletech.vn/wp-content/uploads/2020/11/5b9eb02872831d29ba6e4d5ea0074a27.jpg",
      },
    ],
    mobile: [
      {
        title: "Mobile",
        image:
          "https://cdn.dribbble.com/users/1615584/screenshots/16728853/media/9b4ecd00d1ec6c2003332c0c889d7c1a.jpg?compress=1&resize=1200x900&vertical=top",
      },
      {
        title: "Mobile",
        image:
          "https://cdn.dribbble.com/users/22691/screenshots/17126617/media/1d98fc7e49216e3b99cacc7995912a26.jpg?compress=1&resize=1200x900&vertical=top",
      },
      {
        title: "Mobile",
        image:
          "https://cdn.dribbble.com/users/257709/screenshots/16290615/media/d56b8456ba0f807b023bbf5916014a91.png?compress=1&resize=1200x900&vertical=top",
      },
      {
        title: "Mobile",
        image:
          "https://cdn.dribbble.com/users/26642/screenshots/16152316/media/10f16005ef7b443c75c683fab0713a53.png?compress=1&resize=1200x900&vertical=top",
      },
      {
        title: "Mobile",
        image:
          "https://cdn.dribbble.com/users/1615584/screenshots/14973122/media/347fdfd34ad38b7d5bf0cb690d66dd10.jpg?compress=1&resize=1200x900&vertical=top",
      },
    ],
    publi: [
      {
        title: "Publi",
        image:
          "https://cdn.dribbble.com/users/452635/screenshots/8957076/media/cc14caaca26575317ba9def84bfa5bf4.png?compress=1&resize=1200x900&vertical=top",
      },
      {
        title: "Publi",
        image:
          "https://cdn.dribbble.com/users/2064121/screenshots/15595531/media/0aa6f100d6dc369e5524f4aa14b7dcec.png?compress=1&resize=1200x900&vertical=top",
      },
      {
        title: "Publi",
        image:
          "https://cdn.dribbble.com/users/2064121/screenshots/17122307/media/58b82aabbc1c1cece254ad2746a710b8.jpg?compress=1&resize=1200x900&vertical=top",
      },
      {
        title: "Publi",
        image:
          "https://cdn.dribbble.com/users/371199/screenshots/17227885/media/e6b3b49f269e3ef83bb5a9db8284742e.png?compress=1&resize=1200x900&vertical=top",
      },
    ],
  }),
};
</script>

<style scoped>
.responsiveness {
  display: flex;
}
@media (max-width: 968px) {
  .responsiveness {
    flex-direction: column;
  }
}
</style>
