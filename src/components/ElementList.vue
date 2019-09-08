<template>
  <v-container>
    <v-row
      justify="center"
    >
        <v-col
          cols="12"
          sm="12"
          md="6"
          lg="4"
          xl="3"
          v-for="element in elements"
          :key="element.id"
        >
          <v-card
            hover
          >
            <v-card-title class="card-title">{{ element.name }}</v-card-title>
            <v-card-text class="card-intro">{{ element.introduction }}</v-card-text>
            <v-card-text>作者: {{ element.author }}</v-card-text>
            <v-btn
              text
              v-bind:href="element.url"
              target="_blank"
            >
              <v-icon>mdi-send</v-icon> 点击以访问
            </v-btn>
          </v-card>
        </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'Elementlist',
  components: {
  },
  data: () => ({
    elements: null
  }),
  mounted () {
    this.$axios
      .get('http://127.0.0.1:8000/cards/get/')
      .then(response => (this.elements = response.data))
  }
};
</script>

<style>
  .card-title
  {
    background-color: #00E5FF;
    color: black;
  }
  .card-intro
  {
    margin-top: 10px;
  }
</style>