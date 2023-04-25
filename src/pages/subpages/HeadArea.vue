<template>
  <div class="row">

    <q-parallax :height="660" :speed="0.5">
      <template v-slot:media>
        <img src="~assets/laptop.jpg" width="1400">
      </template>

      <template v-slot:content="scope">
        <div
          :style="{
            opacity: 0.55 + (1 - scope.percentScrolled) * 0.55,
            top: (scope.percentScrolled * 80) + 'px',
            left: 0,
            right: 0
          }"
          class="absolute column q-pl-xl"
        >
          <div class="text-white desktop-only q-pb-xl">
            <span class="q-pa-sm cursor-pointer" @click="scrollToJobs">Berufserfahrung</span>
            <span class="q-pa-sm cursor-pointer" @click="scrollToMe">Über mich </span>
            <span class="q-pa-sm cursor-pointer" @click="scrollToProjects">Projekte </span>
            <span class="q-pa-sm cursor-pointer" @click="scrollToHobby">Interessen</span>
            <span class="q-pa-sm cursor-pointer" @click="scrollToContact">Kontakt</span>
          </div>
          <div class="mobile-only" style="height: 150px"></div>
          <h1 class="desktop-only text-white text-weight-bold q-pa-sm q-pt-xl">Katrin Mischok</h1>
          <h1 class="mobile-only text-white text-h2 text-weight-bold q-pa-sm q-pt-xl">Katrin Mischok</h1>
          <div class=" text-white text-h6 q-pa-sm">Freiberufliche <br /> Software-Entwicklerin <br /> seit 2020</div>
          <div class=" q-pa-sm q-pt-lg ">
            <q-btn color="primary" label="Kontakt" @click="scrollToContact" />
          </div>
        </div>
      </template>
    </q-parallax>
  </div>
</template>
<script>
export default {
  name: "HeadArea",
  props: {
    scrollToContact: {},
    scrollToHobby: {},
    scrollToJobs: {},
    scrollToMe: {},
    scrollToProjects: {}
  }
};
</script>
