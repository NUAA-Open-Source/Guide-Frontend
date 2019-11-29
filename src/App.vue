<template>
  <v-app>
    <v-app-bar
      app
      hide-on-scroll
      color="#00B0FF"
      style="color: black"
    >
      <v-toolbar-title class="headline text-uppercase">
        <span style="margin-right: 5px">A2OS</span>
        <span class="font-weight-light">Guide</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn
        text
        href="https://www.a2os.club"
        target="_blank"
      >
        <v-icon>mdi-home</v-icon>
      </v-btn>
      <v-btn
        text
        href="https://github.com/NUAA-Open-Source/"
        target="_blank"
      >
        <v-icon>mdi-github-circle</v-icon>
      </v-btn>
    </v-app-bar>

    <v-content>
      <Greeting/>
      <ElementList/>
    </v-content>

    <v-footer
      app
      color="#e6e6e6"
    >
      <v-layout justify-center>&copy;A2OS 2018-2019 All rights reserved.</v-layout>
    </v-footer>
  </v-app>
</template>

<script>
import Greeting from './components/Greeting';
import ElementList from './components/ElementList';

export default {
  name: 'App',
  components: {
    Greeting,
    ElementList,
  },
  data: () => ({
    //
  }),
};
</script>

<style>
  .bar-btn {
    color: black;
  }
</style>
