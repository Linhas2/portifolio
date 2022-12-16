<template>
  <v-row justify="center">
    <v-dialog v-model="showDialog" persistent max-width="600px">
      
<v-toolbar color="black" dark flat class="cvi-dialog-toolbar">
      <v-toolbar-title>
        <v-text>KEY SKILLS</v-text>
      </v-toolbar-title>
    </v-toolbar>
      <v-card  color="white">
        <v-card-text>
          <v-container>
            <v-row>

              <v-col cols="12" class="pa-1">
                <v-icon
              icon="mdi-language-html5"
              size="large"
              color="orange darken-4"
            />
                <span class="font-weight-medium primary--text"> HTML
                  <v-progress-linear
                    model-value="95"
                    color="orange darken-4"
                    height="10"
                    striped
                  ></v-progress-linear>
                </span>
              </v-col>


              <v-col cols="12" class="pa-1">
                <v-icon
              icon="mdi-language-css3"
              size="large"
              color="blue darken-3"
            />
                <span class="font-weight-medium primary--text"> CSS
                  <v-progress-linear
                    model-value="95"
                    color="blue darken-3"
                    height="10"
                    striped
                  ></v-progress-linear>
                </span>
              </v-col>


              <v-col cols="12" class="pa-1">
                <v-icon
              icon="mdi-vuejs"
              size="large"
              color="green darken-1"
            />
                <span class="font-weight-medium primary--text"> VUEJS
                  <v-progress-linear
                    model-value="85"
                    color="green darken-1"
                    height="10"
                    striped
                  ></v-progress-linear>
                </span>
              </v-col>

            
              <v-col cols="12" class="pa-1">
                <v-icon
              icon="mdi-vuetify"
              size="large"
              color="green darken-1"
            />
                <span class="font-weight-medium primary--text"> VUETIFY
                  <v-progress-linear
                    model-value="85"
                    color="green darken-1"
                    height="10"
                    striped
                  ></v-progress-linear>
                </span>
              </v-col>


              <v-col cols="12" class="pa-1">
                <v-icon
              icon="mdi-alpha-c-box"
              size="large"
              color="purple darken-2"
            />
                <span class="font-weight-medium primary--text"> C++
                  <v-progress-linear
                    model-value="80"
                    color="purple darken-2"
                    height="10"
                    striped
                  ></v-progress-linear>
                </span>
              </v-col>


              <v-col cols="12" class="pa-1">
                <v-icon
              icon="mdi-language-javascript"
              size="large"
              color="yellow accent-4"
            />
                <span class="font-weight-medium primary--text"> JAVASCRIPT
                  <v-progress-linear
                    model-value="75"
                    color="yellow accent-4"
                    height="10"
                    striped
                  ></v-progress-linear>
                </span>
              </v-col>


              <v-col cols="12" class="pa-1">
                <v-icon
              icon="mdi-language-typescript"
              size="large"
              color="yellow accent-4"
            />
                <span class="font-weight-medium primary--text"> TYPESCRIPT
                  <v-progress-linear
                    model-value="75"
                    color="yellow accent-4"
                    height="10"
                    striped
                  ></v-progress-linear>
                </span>
              </v-col>




              <v-col cols="12" class="pa-1">
                <v-icon
              icon="mdi-database-search"
              size="large"
              color="red accent-4"
            />
                <span class="font-weight-medium primary--text"> MYSQL WORKBENCH
                  <v-progress-linear
                    model-value="50"
                    color="red accent-4"
                    height="10"
                    striped
                  ></v-progress-linear>
                </span>
              </v-col>


            </v-row>
          </v-container>
        </v-card-text>

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
    dialogsk: {
      type: Boolean,
      default: false
    },
  },

  computed: {
    showDialog() {
      return this.dialogsk;
    },
  }
};
</script>