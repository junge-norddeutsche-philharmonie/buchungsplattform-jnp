<template>
  <v-row justify="center" align="center">
    <v-img
      src="/kontrabaesse_1.jpg"
      max-height="20vh"
    >
    </v-img>


    <v-col cols="12" sm="8" md="6">
      <p>Willkommen bei 1to1 Concerts! Bli bla blub. Wir freuen uns auf ihren Besuch!</p>

      <p>Hier sind noch ein paar Hinweise zum Buchungsprozess!</p>

      <v-form v-model="valid">
        <v-container>
          <v-row>
            <v-col
              cols="12"
              md="4"
            >
              <v-text-field
                v-model="form.firstname"
                label="Vorname"
                required
              ></v-text-field>
            </v-col>

            <v-col
              cols="12"
              md="4"
            >
              <v-text-field
                v-model="form.lastname"
                label="Nachname"
                required
              ></v-text-field>
            </v-col>

            <v-col
              cols="12"
              md="4"
            >
              <v-text-field
                v-model="form.number"
                label="Telefonnummer"
                required
              ></v-text-field>
            </v-col>

            <v-col
              cols="12"
              md="4"
            >
              <v-text-field
                v-model="form.mail"
                label="E-Mail"
                required
              ></v-text-field>
            </v-col>

          </v-row>

          <v-row>
            <v-col>
              <v-card elevation="2">
                <v-card-title>23.12.2020 15:00</v-card-title>
                <v-card-subtitle>
                  Im Wunderland
                </v-card-subtitle>
                <v-card-actions>
                  <v-btn
                    color="#ed6b6f"
                    text
                  >
                    Auswählen
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-col>
            <v-col>
              <v-card elevation="2">
                <v-card-title>24.12.2020 15:00</v-card-title>
                <v-card-subtitle>
                  Im Wunderland
                </v-card-subtitle>
                <v-card-actions>
                  <v-btn
                    color="#ed6b6f"
                    text
                    @click="nothing"
                  >
                    Auswählen
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-col>
            <v-col>
              <v-card elevation="2">
                <v-card-title>24.12.2020 15:30</v-card-title>
                <v-card-subtitle>
                  Beim Nikolaus
                </v-card-subtitle>
                <v-card-actions>
                  <v-btn
                    color="#ed6b6f"
                    text
                  >
                    Auswählen
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-col>
          </v-row>


          <v-row>
            <v-col>
              <v-checkbox
                v-model="checkbox"
                :label="`Ich erkläre mich mit den Bedingungen einverstanden.`"
              ></v-checkbox>
            </v-col>
          </v-row>

          <v-row>
            <v-col>
              <v-btn
                color="success"
                class="mr-4"
                @click="submit"
              >
                Anmelden (verbindlich?)
              </v-btn>

              <v-btn
                color="error"
                class="mr-4"
                @click="reset"
              >
                Zurücksetzen
              </v-btn>
            </v-col>
          </v-row>
        </v-container>
      </v-form>


    </v-col>
  </v-row>


</template>

<script>
export default {
  name: "1to1hannover",
  data () {
    return {
      form: {
        firstname: "",
        lastname: "",
        number: "",
        email: "",
        selected: "",
      }
    }
  }
}
</script>

<style scoped>

</style>
