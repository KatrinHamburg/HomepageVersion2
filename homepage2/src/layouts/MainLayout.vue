<template>
  <q-layout view="hhh LpR fff">
    <q-page-container>
      <div class="bg-page">
        <div class="main-container">
        <router-view />
        </div>
      </div>
    </q-page-container>

    <q-footer elevated class="bg-primary text-white">
      <q-toolbar>
        <q-toolbar-title class="text-center">

            <q-btn percentage="0" to="/imprint" class="impress no-focus no-shadow text-subtitle2" label="Impressum"/>
          <q-btn percentage="0" to="/privacy" class="impress no-focus no-shadow text-subtitle2" label="Datenschutz"/>
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>

  </q-layout>
</template>

<script>
export default {
  data () {
    return {
      left: false
    }
  }
}
</script>
<style>
body.desktop .no-focus.q-focusable:focus .q-focus-helper,
body.desktop .no-focus.q-hoverable:hover .q-focus-helper {
background: inherit;
opacity: 0;
}
body.ios .no-focus.q-hoverable:active .q-focus-helper {
background: inherit;
opacity: 0;
}
.no-focus.q-focus-helper {
opacity: 0;
transition: unset;
}
.main-container {
  max-width: 1200px;
  margin-left: auto;
  margin-right: auto;
}
.bg-page {
  background-color: #809DA5
   /*#837877;*/
}
.impress .q-btn__wrapper:before {
  box-shadow: none;
}
</style>
