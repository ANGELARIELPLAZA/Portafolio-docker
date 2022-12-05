<template>
    <v-container grid-list-xl>
      <h2 class="pl-4">
        <span>PCB</span>
        <span class="light-blue--text"> Portafolio</span>
      </h2>
      <v-layout row justify-center align-center wrap class="mt-4 pt-2">
        <v-dialog
          v-model="image.dialog"
          lazy
          max-width="800"
          v-for="image in images"
          :key="image.title"
        >
          <template v-slot:activator="{ on }">
            <v-flex xs12 sm6 md4 lg4 xl4 v-on="on">
              <v-card hover flat color="transparent">
                <v-img
                  :src="image.poster"
                  height="230"
                  :alt="image.title"
                  lazy-src="https://cdn.dribbble.com/users/503653/screenshots/3143656/fluid-loader.gif"
                ></v-img>
                <v-card-title primary-title class="justify-center">{{image.title}}</v-card-title>
              </v-card>
            </v-flex>
          </template>
          <v-card v-if="image.dialog">
            <v-img :src="image.poster"></v-img>
          </v-card>
        </v-dialog>
      </v-layout>
    </v-container>
  </template>
  
  <script>
  export default {
    metaInfo: {
      title: "PCB Portfolio ",
      titleTemplate: "%s ← Angel Ariel",
      meta: [
        { name: "viewport", content: "width=device-width, initial-scale=1" },
        {
          name: "description",
          content:
            "Angel Ariel Graphic Adobe PhotoShop Logo Design Instagram Poster"
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
            "Angel Ariel Graphic Adobe PhotoShop Logo Design Instagram Poster"
        }
      ]
    },
    data() {
      return {
        dialog: false,
        images: [
          {
            dialog: false,
            title: "Placa IoT RGB",
            poster: "https://i.imgur.com/agElJjL.jpg"
          },
          {
            dialog: false,
            title: "Placa IoT",
            poster: "https://i.imgur.com/J60h5sx.jpg"
          }
        ]
      };
    }
  };
  </script>
  
  <style  scoped>
  </style>