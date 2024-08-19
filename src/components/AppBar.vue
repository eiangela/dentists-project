<template>
  <v-app-bar :elevation="1" class="teste-colunas">
    <img src="../assets/images/default-logo.png" class="logo-image" alt="Imagem do Logo" />

    <template v-slot:append>
      <v-app-bar-nav-icon class="nav-icon-right"></v-app-bar-nav-icon>
    </template>
  </v-app-bar>
</template>
