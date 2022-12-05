<template>
  <v-layout row justify-center align-center wrap class="mt-4 pt-2">
    <v-flex xs12 sm12 md5 lg6 xl6 class="mt-4 pt-4">
      <h2 class="mb-4 pl-4 pt-2">Educacion</h2>
      <v-card-text class="py-0">
        <v-timeline align-top dense>
          <v-timeline-item color="cyan darken-1" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">JAN 2018 -</div>
                <div class="caption font-weight-bold green--text">PRESENT</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Full Stack Web Development Course</strong>
                <div class="caption mb-2">freeCodeCamp</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>

          <v-timeline-item color="cyan darken-1" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">SEP 2007 -</div>
                <div class="caption font-weight-bold green--text">MAY 2014</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Telecommunications Engineering</strong>
                <div class="caption mb-2">University of East Sarajevo</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>

          <v-timeline-item color="cyan darken-1" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">SEP 2003 -</div>
                <div class="caption font-weight-bold green--text">MAY 2007</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Electrical Technician for Computers</strong>
                <div class="caption mb-2">Electro-technical school Doboj</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>
        </v-timeline>
      </v-card-text>
    </v-flex>
    <v-flex xs12 sm12 md4 lg6 xl6 class="mt-4 pt-2">
      <h2 class="mb-4 pl-4">Experiencia</h2>
      <v-card-text class="py-0">
        <v-timeline align-top dense>
          <v-timeline-item color="cyan darken-1" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">DEC 2016 -</div>
                <div class="caption font-weight-bold green--text">PRESENT</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Freelance Frontend Developer</strong>
                <div class="caption mb-2">Remote</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>

          <v-timeline-item color="cyan darken-1" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">FEB 2018 -</div>
                <div class="caption font-weight-bold green--text">JULY 2018</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Teacher for electrical technicians</strong>
                <div class="caption mb-2">High School Doboj Istok</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>

          <v-timeline-item color="cyan darken-1" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">AUG 2014 -</div>
                <div class="caption font-weight-bold green--text">APR 2016</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>IT Technician</strong>
                <div class="caption mb-2">MFS-EMMAUS</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>
        </v-timeline>
      </v-card-text>
    </v-flex>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-flex xs12 sm12 md4 lg5 xl5 class="mx-2 pt-4">
        <h2>
          <span>Habilidades de </span>

          <span class="deep-purple--text text--lighten-1">Diseño</span>
        </h2>
        <br>
        <strong>SolidWork</strong>
        <v-progress-linear v-model="buffer1" :buffer-value="bufferValue" color="deep-purple accent-1" height="16"></v-progress-linear>
        <strong>EasyEda</strong>
        <v-progress-linear v-model="buffer2" :buffer-value="bufferValue" color="deep-purple accent-1" height="16"></v-progress-linear>
        <strong>Figma</strong>
        <v-progress-linear v-model="buffer2" :buffer-value="bufferValue" color="deep-purple accent-1" height="16"></v-progress-linear>
      </v-flex>
      <v-flex xs12 sm12 md4 lg5 xl5 class="mx-2 pt-4">
        <h2>
          <span>Habilidades de </span>
          <span class="deep-purple--text text--lighten-1">Programacion</span>
        </h2>
        <br>
        <strong>VUE/NUXT</strong>
        <v-progress-linear v-model="buffer6" :buffer-value="bufferValue" color="deep-purple accent-1" height="16"></v-progress-linear>
        <strong>HTML/CSS/JavaScript</strong>
        <v-progress-linear v-model="buffer3" :buffer-value="bufferValue" color="deep-purple accent-1" height="16"></v-progress-linear>
        <strong>C++/Python</strong>
        <v-progress-linear v-model="buffer1" :buffer-value="bufferValue" color="deep-purple accent-1" height="16"></v-progress-linear>
      </v-flex>
      <div class="mt-4 pt-2">
        <v-btn
          href="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/981ba8bf-fd19-479d-ac92-f92a5f3d303a/CV.pdf?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20221201%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20221201T062814Z&X-Amz-Expires=86400&X-Amz-Signature=84dc2a9b97cbf2a2fe2871a74fb4723e9663da7f9dc2f849b3dd5387431d6595&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22CV.pdf%22&x-id=GetObject"
          target="_blank"
          color="deep-purple lighten-1"
          dark
          large
        >
          Descargar Resumen CV
          <v-icon right dark>fas fa-file-download</v-icon>
        </v-btn>
      </div>
    </v-layout>
  </v-layout>
</template>

<script>
export default {
  metaInfo: {
    title: "Resume",
    titleTemplate: "%s ← Angel Space",
    meta: [
      { name: "viewport", content: "width=device-width, initial-scale=1" },
      {
        name: "description",
        content:
          "Vue NUXT HTML CSS JavaScript Design Adobe XD Photoshop Coding Skills Resume Work Web Developer Front-End"
      },
      { charset: "utf-8" },
      { property: "og:title", content: "Angel Space" },
      { property: "og:site_name", content: "Angel Space" },
      { property: "og:type", content: "website" },
      { property: "og:url", content: "https://Angel.space" },
      {
        property: "og:image",
        content: "https://i.imgur.com/cQLNSuj.jpg"
      },
      {
        property: "og:description",
        content:
          "Vue NUXT HTML CSS JavaScript Design Adobe XD Photoshop Coding Skills Resume Work Web Developer Front-End"
      }
    ]
  },
  data() {
    return {
      value: 0,
      buffer1: 0,
      buffer2: 0,
      buffer3: 0,
      buffer4: 0,
      buffer5: 0,
      buffer6: 0,
      bufferValue: 100,
      interval: 0
    };
  },
  mounted() {
    this.startBuffer();
  },

  beforeDestroy() {
    clearInterval(this.interval);
  },

  methods: {
    startBuffer() {
      this.interval = setInterval(() => {
        this.buffer1 = 90;
        this.buffer2 = 85;
        this.buffer3 = 80;
        this.buffer4 = 80;
        this.buffer5 = 90;
        this.buffer6 = 70;
      }, 800);
    }
  }
};
</script>
<style >
</style>

