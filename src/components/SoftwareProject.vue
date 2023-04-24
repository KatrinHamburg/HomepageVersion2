<template>
  <div class="column justify-center">

    <div class="col-12 text-h6 text-center q-pa-md-md">
     {{ title }} <br />
    </div>

    <div class="row items-center q-mb-xl">

      <div class="col-12 col-md-6 q-pa-xs-xs q-pa-sm-sm q-pa-md-md q-pa-lg-lg q-pa-xl-xl items-center">
        <div class="text-subtitle2 q-pt-md">
          Branche: {{ sector }}
        </div>

        <div class="text-subtitle2 q-pt-sm">
          Methodiken:  {{ methods }}
        </div>

        <div class="text-subtitle2 q-pt-sm">
          Technologien: {{ technologies }}<br />
        </div>

        <div class="q-pt-md">
          {{ shortDescription }}
        </div>

        <div class="q-pt-md">
          {{ description }}
        </div>

      </div>
      <div class="gt-sm col-md-6 q-pa-lg text-center">
        <q-img :src="imageSrc" :style="imageStyle" />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'SoftwareProject',
  props: {
    title: {
      type: String,
      required: true
    },
    sector: {
      type: String,
      required: true
    },
    methods: {
      type: String,
      required: true
    },
    technologies: {
      type: String,
      required: true
    },
    shortDescription: {
      type: String,
      required: true
    },
    description: {
      type: String,
      required: true
    },
    imageSrc: {
      type: String,
      required: true
    },
    imageStyle: {
      type: String,
      required: true
    }
  }
};
</script>
