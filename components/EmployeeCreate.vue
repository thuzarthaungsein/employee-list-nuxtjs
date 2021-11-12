<template>
  <v-row>
    <v-dialog v-model="dialog" persistent max-width="700px" >
      <template v-slot:activator="{ on, attrs }">
        <!-- <v-btn color="primary" dark v-bind="attrs" v-on="on" >
          Create New
        </v-btn> -->

        <v-btn class="mx-2" fab dark color="indigo" v-bind="attrs" v-on="on">
            <v-icon dark>
                mdi-plus
            </v-icon>
        </v-btn>
      </template>
      <v-card>
        <v-card-title>
          <span class="text-h5">New Employee</span>
        </v-card-title>
        <v-card-text>
          <v-container>
            <v-row>
                <v-col cols="12">
                    <label for="">E0101</label>
                </v-col>
              <v-col cols="12" md="6" >
                <v-text-field
                  label="First name"
                ></v-text-field>
              </v-col>
              <v-col cols="12" md="6" >
                <v-text-field label="Last name*" hint="This field required" required ></v-text-field>
              </v-col>
              <v-col cols="12">
                <v-text-field label="Email" ></v-text-field>
              </v-col>
              <v-col cols="12">
                <v-text-field label="Phone Number" type="text" ></v-text-field>
              </v-col>
              <v-col cols="12">
                <v-radio-group v-model="row" row>
                <v-radio label="Male" value="radio-1" ></v-radio>
                <v-radio label="Female" value="radio-2" ></v-radio>
                </v-radio-group>
              </v-col>
              
              <!-- <v-col cols="12">
                <v-textarea label="Address" type="text" rows="1"></v-textarea>
              </v-col> -->
            </v-row>
          </v-container>
          <!-- <small>* indicates required field</small> -->
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn color="blue darken-1" text @click="dialog = false" >
            Close
          </v-btn>
          <v-btn color="blue darken-1" text @click="dialog = false" >
            Save
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-row>
</template>

<script>
  export default {
    data: () => ({
      dialog: false,
    }),
  }
</script>

<style scoped>
.v-text-field .v-label {
    font-size: 12px!important;
}
</style>