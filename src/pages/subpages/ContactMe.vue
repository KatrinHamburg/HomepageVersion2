<template>
  <div class="col bg-secondary text-primary" style="min-height: 100px">
    <div class="q-pa-lg row justify-center">
      <div class="q-pa-sm text-center">
        <q-btn :size="sm" round color="primary" text-color="white" icon="email" @click="mail">
        </q-btn>

      </div>
      <div class="q-pa-sm text-center">
        <q-btn type="a" round href="https://www.xing.com/profile/Katrin_Mischok" target="_blank">
          <q-avatar size="42px">
            <img src="~assets/xing.png">
          </q-avatar>
        </q-btn>
      </div>
      <div class="q-pa-sm text-center">
        <q-btn type="a" round color="primary" href="https://www.linkedin.com/in/katrin-mischok" target="_blank">
          <q-avatar size="42px">
            <img src="~assets/linked-in.png">
          </q-avatar>
        </q-btn>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "ContactMe",
  props: {
    mail: {},
    sm: {}
  }
};
</script>
