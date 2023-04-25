<template>
  <div class="column q-pa-sm">
    <div class="col bg-white q-pt-xl q-pb-xl" style="min-height: 400px">
      <div class="flex flex-center text-block-headline text-block-bold text-primary">Berufserfahrung</div>
      <div class="flex flex-center text-primary  q-pb-lg">Rollen & Verantwortlichkeiten</div>
      <div class="row">
        <div class="col-xs-12 col-sm-4 q-pa-sm">
          <q-card class=" bg-secondary q-pa-sm" flat square style="height: 100%">
            <q-card-section>
              <div class="text-subtitle2">März 2016 - April 2020</div>
              <div class="text-h6 q-pt-sm text-primary text-block-bold">Immowelt Hamburg GmbH</div>
            </q-card-section>

            <q-card-section class="q-pt-none">
              In der Rolle als Full Stack Developer entwickelten wir als Scrum-Team ein neues Produkt für das
              Unternehmen.
            </q-card-section>
          </q-card>
        </div>
        <div class="col-xs-12 col-sm-4 q-pa-sm">
          <q-card class=" bg-secondary q-pa-sm" flat square style="height: 100%">
            <q-card-section>
              <div class="text-subtitle2">Januar 2010 - Februar 2016</div>
              <div class="text-h6 q-pt-sm text-primary text-block-bold">Monday Consulting GmbH</div>
            </q-card-section>

            <q-card-section class="q-pt-none">
              Als Software-Entwicklerin, Projektleiterin und Scrum Master war ich in mehreren Kundenprojekten tätig.
              Ich konzipierte und entwickelte Applikationen, erstellte Projektpläne, überwachte den Projektfortschritt
              und entwickelte Wireframes.
            </q-card-section>
          </q-card>
        </div>
        <div class="col-xs-12 col-sm-4 q-pa-sm">
          <q-card class="bg-secondary q-pa-sm" flat square style="height: 100%">
            <q-card-section>
              <div class="text-subtitle2">Mai 2007 - Dezember 2009</div>
              <div class="text-h6 q-pt-sm text-primary text-block-bold">Capgemini sd&m</div>
            </q-card-section>
            <q-card-section class="q-pt-none">
              In verschiedenen Projekten war ich für die Konzeption und Implementierung von kundenindividuellen
              IT-Lösungen verantwortlich. In einigen Projekten übernahm ich die fachliche Führung der
              Projektmitarbeiter.
            </q-card-section>
          </q-card>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "WorkExperience"
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
