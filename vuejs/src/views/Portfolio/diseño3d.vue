<template>
  <v-container grid-list-xl>
    <h2 class="pl-4">
      <span>Diseño</span>
      <span class="light-blue--text"> 3D</span>
    </h2>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-dialog
        v-model="video.dialog"
        lazy
        max-width="800"
        v-for="video in videos"
        :key="video.title"
      >
        <template v-slot:activator="{ on }">
          <v-flex xs12 sm6 md4 lg4 xl4 v-on="on">
            <v-card hover flat color="transparent">
              <v-img
                :src="video.poster"
                aspect-ratio="1.7778"
                :alt="video.title"
                lazy-src="https://cdn.dribbble.com/users/503653/screenshots/3143656/fluid-loader.gif"
                contain
              ></v-img>
              <v-card-title primary-title class="justify-center">{{video.title}}</v-card-title>
            </v-card>
          </v-flex>
        </template>
        <v-card v-if="video.dialog">
          <plyr>
            <div class="plyr__video-embed">
              <iframe :src="video.href" allowfullscreen allowtransparency allow="autoplay"></iframe>
            </div>
          </plyr>
        </v-card>
      </v-dialog>
    </v-layout>
  </v-container>
</template>

<script>
import { PlyrVideo } from "vue-plyr";

export default {
  metaInfo: {
    title: "3D Portfolio",
    titleTemplate: "%s ← Angel Ariel",
    meta: [
      { name: "viewport", content: "width=device-width, initial-scale=1" },
      {
        name: "description",
        content:
          "Angel Ariel Services Adobe Premire After Effects Video Ad's Social Media Logo Animation Instagram Facebook Video Editing Advetising"
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
          "Angel Ariel Services Adobe Premire After Effects Video Ad's Social Media Logo Animation Instagram Facebook Video Editing Advetising"
      }
    ]
  },
  components: { plyr: PlyrVideo },
  data() {
    return {
      dialog: false,
      videos: [
        {
          dialog: false,
          title: "PRENSA",
          href: "",
          type: "text/html",
          youtube: "",
          poster: "https://i.imgur.com/vyhW7s3.png"
        },
        {
          dialog: false,
          title: "ARBOL EOLICO",
          href: "",
          type: "text/html",
          youtube: "",
          poster: "https://i.imgur.com/DXX8SQG.png"
        },
        {
          dialog: false,
          title: "CASE 3D",
          href: "",
          type: "text/html",
          youtube: "",
          poster: "https://i.imgur.com/JIE87ji.png"
        },
        {
          dialog: false,
          title: "SISTEMA HIDROPONICO",
          href: "",
          type: "text/html",
          youtube: "",
          poster: "https://i.imgur.com/7gtyaTQ.jpg"
        },
        {
          dialog: false,
          title: "CONCEPTO DE SISTEMA EMBEBIDO IoT",
          href: "",
          type: "text/html",
          youtube: "",
          poster: "https://i.imgur.com/kdej6ZU.png"
        }
        ,
        {
          dialog: false,
          title: "Dispensador IoT",
          href: "",
          type: "text/html",
          youtube: "",
          poster: "https://i.imgur.com/kybn1AD.png",
        }
      ]
    };
  }
};
</script>

<style  scoped>
@import "../../../node_modules/vue-plyr/dist/vue-plyr.css";
</style>