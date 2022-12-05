<template>
  <v-layout column justify-center align-center class="mt-4 pt-2">
    <VueCompareImage class="hidden-md-and-down" hover :style="{ minWidth: '1300px' }" :sliderLineWidth="sliderLine"
      :handleSize="hSize" :leftImage="leftImage" :rightImage="rightImage" :sliderPositionPercentage="sliderPosition" />
    <VueCompareImage class="hidden-lg-and-up" hover :style="{ maxWidth: '400px' }" :sliderLineWidth="sliderLine"
      :handleSize="hSize" :leftImage="leftImage2" :rightImage="rightImage2"
      :sliderPositionPercentage="sliderPosition" />

    <br>

    <vue-typer class="headline" :repeat="0" text="Angel Ariel"></vue-typer>
    <vue-typer :text="text1" :repeat="Infinity" :shuffle="false" initial-action="erasing" :pre-type-delay="70"
      :type-delay="70" :pre-erase-delay="1980" :erase-delay="150" erase-style="select-back" :erase-on-complete="false"
      caret-animation="smooth"></vue-typer>
    <br>
    <v-flex xs12 sm6 md4 lg4 xl4>
      <v-card flat color="transparent" max-width="500">
        <v-card-title primary-title class="justify-center">
          <div>
            <h3 class="headline mb-0">
              <span>Sobre</span>
              <span class="light-blue--text">Mi</span>
            </h3>
            <div>
              <p>
                ¡Hola! Soy Ángel Ariel. Soy <span class="light-blue--text font-weight-bold">desarrollador IoT e Ing.Electronico </span> que
                esta apasionado por el desarrollo web/dispositivos en sistemas ciberfisicos creando plataformas simples y
                conectandolas al mundo real.
                <br>
                Tengo muchos pasatiempos pero mi objetivo es superarme dia con dia ya sea programando, editando,
                creando, diseñando o incluso reparando, una de mis metas es viajar y conocer el mundo sin dejar de
                aprender.
              </p>
            </div>
          </div>
        </v-card-title>

        <v-card-actions class="hidden-sm-and-down justify-center">
          <v-btn v-for="icon in icons" :key="icon.icon" fab dark outline color="blue" :href="icon.href" target="_blank">
            <v-icon dark>{{ icon.icon }}</v-icon>
          </v-btn>
        </v-card-actions>

        <v-card-actions class="hidden-md-and-up justify-center">
          <v-btn v-for="icon in icons" :key="icon.icon" small fab dark outline color="blue" :href="icon.href"
            target="_blank">
            <v-icon dark>{{ icon.icon }}</v-icon>
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
import { VueTyper } from "vue-typer";
import VueCompareImage from "vue-compare-image";

export default {
  metaInfo: {
    title: "Home",
    titleTemplate: "%s ← Angel Ariel",
    meta: [
      { name: "viewport", content: "width=device-width, initial-scale=1" },
      { name: "description", content: "Angel Ariel Portfolio" },
      { charset: "utf-8" },
      { property: "og:title", content: "Angel" },
      { property: "og:site_name", content: "Angel" },
      { property: "og:type", content: "website" },
      { property: "og:url", content: "" },
      {
        property: "og:image",
        content: "https://i.imgur.com/cQLNSuj.jpg"
      },
      { property: "og:description", content: "Angel Ariel Portfolio" }
    ]
  },
  components: {
    "vue-typer": VueTyper,
    VueCompareImage
  },
  data() {
    return {
      icons: [
        { href: "https://github.com/ANGELARIELPLAZA", icon: "fab fa-github" },
        {
          href: "https://www.linkedin.com/in/angel-ariel-plaza-acu%C3%B1a-a15567217/",
          icon: "fab fa-linkedin-in"
        },
        {
          href: "https://www.facebook.com/ary.anllel.5",
          icon: "fab fa-facebook-f"
        },
        { href: "https://www.instagram.com/dev_iiot3d/", icon: "fab fa-instagram" }
      ],
      text1: [" FullStack Jr Developer", "IoT Developer", "Web Designer" ,"Ing.Electronico"],
      leftImage: "https://i.imgur.com/lthRftA.png",
      rightImage: "https://i.imgur.com/sfEnWJ3.png",
      leftImage2: "https://i.imgur.com/Rv5fZ7B.png",
      rightImage2: "https://i.imgur.com/Rv5fZ7B.png",
      sliderLine: 0,
      hSize: 0,
      sliderPosition: 0.5
    };
  }
};
</script>
<style>
@keyframes rocking {

  0%,
  100% {
    transform: rotateZ(-10deg);
  }

  50% {
    transform: rotateZ(10deg);
  }
}

.vue-typer {
  font-family: Arial, "Helvetica Neue", Helvetica, sans-serif;
}

.vue-typer .custom.char.typed {
  color: #76DDFD;
}

.vue-typer .custom.char.selected {
  color: #000000;
}

.vue-typer .custom.caret {
  animation: rocking 1s ease-in-out 0s infinite;
}

.vue-typer .custom.caret.typing {
  background-color: #76DDFD;
}

.vue-typer .custom.caret.selecting {
  display: inline-block;
  background-color: #e91e63;
}
</style>

