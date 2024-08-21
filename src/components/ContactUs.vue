Pq minha foto não pega o container pai? gostaria que ela pegasse 100% do espaço do container pai

<template>
  <div class="d-flex flex-column flex-md-row mt-6 mb-6 mt-sm-10 mt-md-10">
    <div class="contact-image mb-sm-10"></div>

    <v-container>
      <v-row class="d-flex flex-column justify-center ml-md-16 pa-6">
        <h1 class="text-h3 text-center text-md-start font-weight-bold mb-5">Contact Us</h1>
        <v-col cols="12" sm="12" md="12" lg="12" xl="6">
          <div>
            <div>
              <div class="form-field-label">Nome</div>
              <v-text-field
                variant="underlined"
                density="compact"
                placeholder="Enter your Name"
                required
              ></v-text-field>
            </div>
          </div>
        </v-col>

        <v-col cols="12" sm="12" md="12" lg="12" xl="6">
          <div>
            <div>
              <div class="form-field-label">E-mail</div>
              <v-text-field
                variant="underlined"
                density="compact"
                placeholder="Enter a valid email adress"
                required
              ></v-text-field>
            </div>
          </div>
        </v-col>

        <v-col cols="12" sm="12" md="12" lg="12" xl="6">
          <div>
            <div>
              <div class="form-field-label">Mensagem</div>
              <v-textarea variant="underlined"></v-textarea>
            </div>
          </div>
        </v-col>

        <v-col cols="12" sm="12" md="12" lg="12" xl="6">
          <v-checkbox v-model="checkbox">
            <template v-slot:label>
              <div>
                I accept the
                <v-tooltip location="bottom">
                  <template v-slot:activator="{ props }">
                    <a
                      href="https://vuetifyjs.com"
                      class="text-decoration-none"
                      target="_blank"
                      v-bind="props"
                      @click.stop
                    >
                      <span class="contact-terms"> Terms of Service </span>
                    </a>
                  </template>
                </v-tooltip>
              </div>
            </template>
          </v-checkbox>
        </v-col>

        <v-col cols="12" sm="12" md="12" lg="12" xl="6">
          <div>
            <v-btn
              class="btn-contact font-weight-bold text-h6 text-uppercase"
              block
              variant="flat"
              height="66"
            >
              Submit
            </v-btn>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </div>

  <v-container width="1280">
    <v-row>
      <v-col v-for="(infos, i) in informations" :key="i" cols="12" sm="12" md="4">
        <v-card height="200" variant="variant" class="bgn-color d-flex flex-column justify-center">
          <v-card-title class="mb-0 ml-10 text-md-h5"> {{ infos.infoTitle }} </v-card-title>
          <v-card-text class="flex-grow-0 ml-10 text-md-h6"> {{ infos.infoNumber }} </v-card-text>
          <v-card-text class="flex-grow-0 ml-10 text-md-h6"> {{ infos.infoNumber2 }} </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
import { ref } from 'vue'

const checkbox = ref(false)

const informations = [
  {
    infoTitle: 'Call us',
    infoNumber: '(11) 6666-9999',
    infoNumber2: '(11)9999-9999'
  },
  {
    infoTitle: 'Location',
    infoNumber: '121 Rock Sreet, 21 Avenue, New York',
    infoNumber2: '92103-9000'
  },
  {
    infoTitle: 'Hours',
    infoNumber: 'Mon - Fri ....... 11 am - 8pm, Sat, Sun.....',
    infoNumber2: '6am - 8am - 9am'
  }
]
</script>
