<template>
  <div class="col bg-primary" style="min-height: 400px">
    <div class="q-pa-lg q-pt-xl text-center text-block-bold text-block-headline text-white ">Interessen & Hobbys</div>

    <div class="row q-pa-lg">
      <div class="col-xs-12 col-sm-4 q-pa-sm text-center">
        <q-avatar size="180px">
          <img src="~assets/foosball.jpg">
        </q-avatar>
        <div class="text-white text-h6 q-pa-md">Kickern</div>
      </div>
      <div class="col-xs-12 col-sm-4 q-pa-sm text-center">
        <q-avatar size="180px">
          <img src="~assets/book.jpg">
        </q-avatar>
        <div class="text-white text-h6 q-pa-md">Lesen</div>
      </div>
      <div class="col-xs-12 col-sm-4 q-pa-sm text-center">
        <q-avatar size="180px">
          <img src="~assets/family.jpg">
        </q-avatar>
        <div class="text-white text-h6 q-pa-md">Familie</div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "HobbyArea"
};
</script>
<style>


.text-block-headline {
  font-size: 40px;
}

.text-block-bold {
  font-weight: 700;
}

</style>
