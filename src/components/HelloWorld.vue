<template>
  <v-container fluid class="fill-height banana">
    <div class="bordatop">
      <v-img
        contain
        height="350"
        src="https://camo.githubusercontent.com/61491d59e71fec5c794945fed916a4a682b6c0404fc31f30b08a0d919c558404/68747470733a2f2f696d616765732e73717561726573706163652d63646e2e636f6d2f636f6e74656e742f76312f3537363966633430316236333162616231616464623261622f313534313538303631313632342d5445363451474b524a4738535741495553374e532f6b6531375a77644742546f6464493870446d34386b506f73776c7a6a53564d4d2d53784f703743563539425a772d7a505067646e346a557756634a45315a7657515578776b6d794578676c4e714770304976544a5a616d574c49327a76595748384b332d735f3479737a63703272795449304871544f6161556f68724938504936465879386339505774426c7141566c555335697a7064634958445a71445976707252715a32395077306f2f636f64696e672d667265616b2e676966"
      />
    </div>

      <div class="text-body-2 font-weight-light mb-n1 d-flex align-center justify-center">Portifolio of</div>
      <h1 class="text-h2 font-weight-bold d-flex align-center justify-center">Guilherme Linhares</h1>

      <v-row class="d-flex align-center justify-center bordatop2">
        <v-col cols="auto">
          <v-btn
            min-width="164"
            rel="noopener noreferrer"
            target="_blank"
            variant="text"
            @click="showdialogexp=true"
          >
            <v-icon
              icon="mdi-newspaper-variant-multiple"
              size="large"
              start
            />

            Experiences
          </v-btn>
        </v-col>

        <v-col cols="auto">
          <v-btn
            color="black"
            min-width="228"
            rel="noopener noreferrer"
            size="x-large"
            target="_blank"
            variant="flat"
            @click="showdialogsk=true"
          >
            <v-icon
              icon="mdi-speedometer"
              size="large"
              start
            />

            Key Skills
          </v-btn>
        </v-col>

        <v-col cols="auto">
          <v-btn
            href="https://github.com/LinhaS2"
            min-width="164"
            rel="noopener noreferrer"
            target="_blank"
            variant="text"
          >
            <v-icon
              icon="mdi-github"
              size="large"
              start
            />
            Github
          </v-btn>
        </v-col>
        <v-col cols="12" class="bordatop3">
          </v-col>
    </v-row>
      <Dialogsk :dialogsk="showdialogsk" @close="showdialogsk = false" />
      <Dialogexp :dialogexp="showdialogexp" @close="showdialogexp = false" />
      <Footer />  
  </v-container>
</template>


<script>
import Footer from '@/components/Footer.vue'
import Dialogsk from '@/components/DialogSkills.vue'
import Dialogexp from '@/components/DialogExp.vue'
  export default {
    components: {
      Footer,
      Dialogsk,
      Dialogexp
    },
    data: () => ({
      showdialogsk:false,
      showdialogexp:false
       }),
       
  }
</script>

<style scoped>
      .banana{
        padding-top: 0;
        padding-bottom: 0;
        padding-left: 0;
        padding-right: 0;
      }

      .bordatop{
        padding-top: 8rem;
      }
      .bordatop2{
        padding-top: 2rem;
      }
      .bordatop3{
        padding-top: 12rem;
      }
</style>