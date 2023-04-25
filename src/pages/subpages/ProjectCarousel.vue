<template>
  <div class="col bg-secondary">

    <div
      class="bg-white q-pa-lg-lg q-pa-sm-sm q-pa-md-md q-pa-xs-md text-center text-block-bold text-block-headline text-primary ">
      Projekte
    </div>

    <q-carousel
      v-model="slide"
      animated
      arrows
      class="bg-secondary text-primary flat"
      control-color="primary"
      height="530px"
      infinite
      navigation
      padding
      swipeable
      transition-next="slide-left"
      transition-prev="slide-right"
    >
      <q-carousel-slide name="prices">
        <SoftwareProject
          description="Im Rahmen einer auf Microservices basierten Architektur wurden Backend-Anwendungen und eine Frontend Applikation in der AWS-Cloud umgesetzt. Ich konzipierte, entwickelte und testete Backend- und Frontend-Funktionalitäten."
          imageSrc="prices.jpg"
          imageStyle="width: 430px"
          methods="Kanban, Scrum, Microservices, Continuous Delivery"
          sector="Handel"
          short-description="Entwicklung verschiedener Microservices, zum Beispiel zur Berechnung von rechtskonformen Streichpreisen."
          technologies="AWS, Spring Boot, Kotlin, React, Kafka, GitHub "
          title=" Neuentwicklung von Services im Bereich Preise"
        />
      </q-carousel-slide>

      <q-carousel-slide name="tenant">
        <SoftwareProject
          description="Im Rahmen einer auf Microservices basierten Architektur wurden eine App, ein Back-Office-System und
                    Backend-Anwendungen in der AWS-Cloud umgesetzt. Ich entwickelte vor allem Backend- Funktionalitäten,
                    aber half auch im Frontend aus. Ich erstellte Unit- und Integrationstests."
          imageSrc="parking.jpg"
          imageStyle="width: 230px"
          methods="Scrum, DDD, Microservices"
          sector="Finanzen"
          short-description="Entwicklung einer Plattform, die verschiedene Nutzungsaspekte kommerzieller Gebäude für den Nutzer bündelt."
          technologies="AWS, Spring Boot, Kotlin, Vue.js "
          title=" Neuentwicklung eines „Mieter-Ökosystems“"
        />
      </q-carousel-slide>

      <q-carousel-slide name="valuation">
        <SoftwareProject
          description="In einem agilen crossfunktionalen Team wurden diverse Microservices entwickelt. Ich übernahm in dem
                    Projekt sowohl Backend- als auch Frontend-Entwicklungen und erstellte Tests.
                    Eine teameigene Continuous Delivery Pipeline wurde aufgebaut."
          imageSrc="valuation.jpg"
          imageStyle="width: 360px"
          methods="Scrum, DDD, Microservices"
          sector="Immobilien"
          short-description="Entwicklung einer Immobilienbewertungsstrecke, Backend-Anwendungen und einem Back-Office-System
                    im Rahmen der Anwendungsdomäne Eigentümerkontakte."
          technologies="Vue.js, Quasar, Java 11, Spring Boot "
          title="Neuentwicklung einer Immobilienbewertung"
        />
      </q-carousel-slide>

      <q-carousel-slide name="realestate">
        <SoftwareProject
          description="Altsysteme wurden durch eine Microservice basierte Architektur abgelöst. Ich entwickelte
                    Backend- und Frontend- Funktionalitäten und half bei der Erstellung einer Continuous Delivery Pipeline."
          imageSrc="realestate.jpg"
          imageStyle="width: 320px"
          methods="Scrum, Schichtenarchitektur, Microservices"
          sector="Immobilien"
          short-description="Entwicklung von Microservices und einer Continuous Delivery Pipeline."
          technologies="Java 8, Thymeleaf, Spring Boot, Gradle, Jenkins, Apache Mesos, DC/OS "
          title="Neuentwicklung einer Startseite eines Immobilienportals"
        />
      </q-carousel-slide>

      <q-carousel-slide name="warehouse">
        <SoftwareProject
          description=""
          imageSrc="warehouse.jpg"
          imageStyle="width: 250px"
          methods="Agile Softwareentwicklung, Schichtenarchitektur"
          sector="Handel"
          short-description="Projektleitung, Konzeptionierung und Entwicklung einer Webanwendung zur Bereitstellung der
                     Warenwirtschaftsprozesse in den Filialen mit direktem Zugriff auf das zentrale SAP-System."
          technologies="Java, JUnit, Spring Boot, SAP Java Connector, JDBC, Maven "
          title="Neuentwicklung eines internationalen Portals zur Abwicklung warenwirtschaftlicher Prozesse"
        />
      </q-carousel-slide>

      <q-carousel-slide name="stocktaking">
        <SoftwareProject
          description=""
          imageSrc="stocktaking.jpg"
          imageStyle="width: 250px"
          methods="Agile Softwareentwicklung, Schichtenarchitektur"
          sector="Handel"
          short-description="Konzeptionierung und Entwicklung eines webgestützten Systems zur Inventurdurchführung für eine Einzelhandelskette. Sowohl Mobile- als auch Desktop-Variante."
          technologies="Java, Spring, Sencha Touch 2, CoreMedia 5.2 "
          title="Entwicklung eines webbasierten Inventursystems"
        />
      </q-carousel-slide>

      <q-carousel-slide name="planning">
        <SoftwareProject
          description=""
          imageSrc="planing.jpg"
          imageStyle="width: 350px"
          methods="Iterative Softwareentwicklung"
          sector="Handel"
          short-description="Neuentwicklung und Konzeptionierung eines Planungssystems für den Non-Food-Bereich eines Handelshauses."
          technologies="C#, Microsoft Visual Studio, MS SQL Server 2005 "
          title="Planungssystem"
        />
      </q-carousel-slide>

    </q-carousel>

  </div>
</template>
<script>

import SoftwareProject from "../../components/SoftwareProject";

export default {
  name: "ProjectCarousel",
  components: { SoftwareProject },
  data() {
    return {
      slide: "prices"
    };
  }
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
