<template>
  <v-row justify="center">
    <v-dialog v-model="showDialog" persistent max-width="600px">
      
<v-toolbar color="black" dark flat class="cvi-dialog-toolbar">
      <v-toolbar-title>
        <v-text>EXPERIENCES</v-text>
      </v-toolbar-title>
    </v-toolbar>

      <v-card  color="white">
        <v-card-text>
          <v-container>
            <v-row>
              I have been working for a year for the city government, in the Municipal Education Secretariat.
Here I am responsible for the maintenance and front-end development of the application called Erudio (school management software in which more than 3 thousand employees and 32 thousand students are managed, distributed over more than 130 school units in the city of Itajaí/SC).
<br>
And also responsible for the maintenance and front-end development of the application called Cadastro Vaga Integral, whose purpose is the management of full-time vacancies in licensed private day-care centers in the city.
            </v-row>
          </v-container>
        </v-card-text>

        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn variant="outlined" color="black" @click="$emit('close')">
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
    dialogexp: {
      type: Boolean,
      default: false
    },
  },

  computed: {
    showDialog() {
      return this.dialogexp;
    },
  }
};
</script>