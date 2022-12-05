<template>
  <v-container grid-list-xl>
    <h2 class="pl-4">
      <span>Web</span>
      <span class="light-blue--text">Portfolio</span>
    </h2>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-dialog
        v-model="project.dialog"
        lazy
        max-width="1000"
        v-for="project in projects"
        :key="project.title"
      >
        <template v-slot:activator="{ on }">
          <v-flex xs12 sm6 md4 lg4 xl4 v-on="on">
            <v-card hover flat color="transparent">
              <v-img
                :src="project.poster"
                :alt="project.title"
                height="230"
                
              ></v-img>
              <v-card-title primary-title class="justify-center">{{project.title}}</v-card-title>
            </v-card>
          </v-flex>
        </template>
        <v-card v-if="project.dialog">
          <v-img :src="project.poster"></v-img>
          <v-card-text>
            <h3 class="headline mb-0">
              <span>Technology</span>
            </h3>
            <v-chip color="green" text-color="white">{{project.tech.tech1}}</v-chip>
            <v-chip color="green" text-color="white">{{project.tech.tech2}}</v-chip>
            <v-chip color="green" text-color="white">{{project.tech.tech3}}</v-chip>
            <v-chip color="green" text-color="white">{{project.tech.tech4}}</v-chip>
          </v-card-text>
          <v-card-actions>
            <v-btn flat large dark color="green" :href="project.git" target="_blank">
              <v-icon left>fab fa-github</v-icon>GitHub
            </v-btn>
            <v-btn large flat dark color="green" :href="project.demo" target="_blank">
              <v-icon left>fas fa-desktop</v-icon>Demo
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  metaInfo: {
    title: "Web Portfolio",
    titleTemplate: "%s ← Angel Ariel",
    meta: [
      { name: "viewport", content: "width=device-width, initial-scale=1" },
      {
        name: "description",
        content:
          "Angel Ariel Web Portfolio Vue Vue.js Nuxt Nuxt.js HTML CSS Vuetify Axios GraphQL JavaScript Web Developer Front-End Frontend Designer App Responsive"
      },
      { charset: "utf-8" },
      { property: "og:title", content: "Angel" },
      { property: "og:site_name", content: "Angel" },
      { property: "og:type", content: "website" },
      { property: "og:url", content: "" },
      {
        property: "og:image",
        content: "https://i.imgur.com/cQLNSuj.jpg"
      },
      {
        property: "og:description",
        content:
          "Angel Ariel Web Portfolio Vue Vue.js Nuxt Nuxt.js HTML CSS Vuetify Axios GraphQL JavaScript Web Developer Front-End Frontend Designer App Responsive"
      }
    ]
  },
  data() {
    return {
      dialog: false,
      projects: [
         {
          dialog: false,
          title: "Tienda online frontend",
          git: "https://github.com/ANGELARIELPLAZA/FrontEnd-Store",
          demo: "https://ecomers-store.netlify.app/",
          tech: {
            tech1: "HTML",
            tech2: "CSS",
            tech3: "GITHUB",
          },
          poster: "https://i.imgur.com/2aIiP1B.png"
        },
        {
          dialog: false,
          title: "Hackaton SIRIUS BOX CHAIN-OBIO",
          git: "https://github.com/ANGELARIELPLAZA/SIRIUS-BOX-CHAIN",
          demo: "https://sirius-box-chain.netlify.app/",
          tech: {
            tech1: "HTML",
            tech2: "CSS",
            tech3: "JS",
            tech4: "GIT"
          },
          poster: "https://i.imgur.com/SZQHURN.png"
        },
        {
          dialog: false,
          title: "HACKATON OMNIGREEN",
          git: "https://github.com/ANGELARIELPLAZA/Hackaton-orizaba",
          demo: " ",
          tech: {
            tech1: "HTML",
            tech2: "CSS",
            tech3: "JS",
            tech4: "LARAVEL"
          },
          poster: "https://i.imgur.com/er5CQ3z.png"
        },
        {
          dialog: false,
          title: "Acuicola IoT",
          git: "https://github.com/ANGELARIELPLAZA/IoT-ITESCO",
          demo: "",
          tech: {
            tech1: "NODE-RED",
            tech2: "EMQTT",
            tech3: "HTML",
            tech4: "DOCKER"
          },
          poster: "https://i.imgur.com/EZt8lTT.png"
        },
        {
          dialog: false,
          title: "ACUICOLA IOT INVESTIGACION",
          git: "https://github.com/ANGELARIELPLAZA/IoT-ITESCO",
          demo: "",
          tech: {
            tech1: "GRAFANA",
            tech2: "INFLUX",
            tech3: "AWS",
            tech4: "DOCKER"
          },
          poster: "https://i.imgur.com/tCk7QgS.jpg"
        },
        {
         
        }
      ]
    };
  }
};
</script>

<style  scoped>
</style>