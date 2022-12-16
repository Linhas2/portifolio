<template>
  <footer class="text-center d-flex flex-column">
      <div>
          <Dialoggmail :dialoggmail="showdialoggmail" @close="showdialoggmail = false" />
        <v-btn
            href="https://www.linkedin.com/in/guilherme-linhares-de-medeiros-76434722b/"
            target="_blank"
            variant="text"
          >
            <v-icon
              icon="mdi-linkedin"
              size="large"
            />
          </v-btn>


          <v-btn
            href="https://www.instagram.com/gui.linharess/"
            target="_blank"
            variant="text"
          >
            <v-icon
              icon="mdi-instagram"
              size="large"

            />
          </v-btn>


          <v-btn
            target="_blank"
            variant="text"
            @click="showdialoggmail=true"
          >
            <v-icon
              icon="mdi-gmail"
              size="large"

            />
          </v-btn>
      </div>

    <v-divider></v-divider>

    <div>
      {{ new Date().getFullYear() }} — made for me
    </div>
    </footer>
</template>

    <script>
import Dialoggmail from '@/components/DialogGmail.vue'
 export default {
    components: {
      Dialoggmail
    },

    data: () => ({
      showdialoggmail:false,
       })
 }
</script>

<style scoped>
      .banana{
        padding-right: 2rem;
        padding-left: 2rem;
      }
</style>