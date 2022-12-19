<template>
  <v-container fluid class="fill-height banana">
    <div class="bordatop">
      <v-img
        contain
        height="350"
        src="src/assets/dev.png"
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