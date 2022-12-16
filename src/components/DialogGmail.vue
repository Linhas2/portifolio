<template>
  <v-row justify="center">
    <v-dialog v-model="showDialog" persistent max-width="600px">
      
<v-toolbar color="black" dark flat class="cvi-dialog-toolbar">
      <v-toolbar-title>
        <v-text>SEND E-MAIL TO ME</v-text>
      </v-toolbar-title>
    </v-toolbar>

<v-card  color="white">
  <v-container>
    <form id="contactForm" data-sb-form-api-token="API_TOKEN" action="https://formsubmit.co/guilhermelinhares2706@gmail.com" method="POST" class="card">
      <input type="hidden" name="accessKey" value="[INSERIR A CHAVE DE ACESSO AQUI]">
        <div> 
          
            <v-text-field
              v-model="name"
              label="Name"
              type="text"
              name="name"
              id="name"
            ></v-text-field>
            <v-text-field
              v-model="email"
              label="E-mail"
              type="email"
              name="email"
              id="email"
            ></v-text-field>
            <v-text-field
              v-model="message"
              label="Message"
              type="text"
              name="message"
              id="email"
            ></v-text-field>
          
        <div>
          <button class="bg-black py-2 px-8 text-white texte">Enviar</button>
        </div>
        </div>
    </form>
  </v-container>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn variant="outlined" color="black" text @click="$emit('close')">
            CLOSE
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-row>
</template>

<script>
export default {
  props: {
    dialoggmail: {
      type: Boolean,
      default: false
    },
  },
  
  data: () => ({
      name: '',
      email: '',
      message: '',
    }),

  computed: {
    showDialog() {
      return this.dialoggmail;
    },
  }
};
</script>

<style scoped>

button{
background: transparent;
transform: translate(0);
overflow: hidden;
cursor: pointer;
}

input{
background: transparent;
padding: 16px  36px;
border: 1px solid #000; 
transform: translate(0);
overflow: hidden;
cursor: pointer;
}
</style>