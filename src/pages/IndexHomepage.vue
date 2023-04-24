<template>
  <q-page class="bg-white">


      <div class="row">

        <q-parallax :height="660" :speed="0.5">
          <template v-slot:media>
            <img src="~assets/laptop.jpg" width="1400">
          </template>

          <template v-slot:content="scope">
            <div
              class="absolute column q-pl-xl"
              :style="{
            opacity: 0.55 + (1 - scope.percentScrolled) * 0.55,
            top: (scope.percentScrolled * 80) + 'px',
            left: 0,
            right: 0
          }"
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
              <div class=" text-white text-h6 q-pa-sm">Freiberufliche <br/> Software-Entwicklerin <br/> seit 2020</div>
              <div class=" q-pa-sm q-pt-lg ">
                <q-btn @click="scrollToContact" color="primary" label="Kontakt"/>
              </div>
            </div>
          </template>
        </q-parallax>
      </div>

      <div ref="jobs" class="column q-pa-sm">
        <div class="col bg-white q-pt-xl q-pb-xl" style="min-height: 400px">
          <div  class="flex flex-center text-block-headline text-block-bold text-primary">Berufserfahrung</div>
          <div class="flex flex-center text-primary  q-pb-lg">Rollen & Verantwortlichkeiten</div>
          <div class="row">
            <div class="col-xs-12 col-sm-4 q-pa-sm">
              <q-card  style="height: 100%" class=" bg-secondary q-pa-sm" flat square>
                <q-card-section>
                  <div class="text-subtitle2">März 2016 - April 2020</div>
                  <div class="text-h6 q-pt-sm text-primary text-block-bold">Immowelt Hamburg GmbH</div>

                </q-card-section>

                <q-card-section class="q-pt-none">
                  In der Rolle als Full Stack Developer entwickelten wir als Scrum-Team ein neues Produkt für das Unternehmen.
                </q-card-section>
              </q-card>
            </div>
            <div class="col-xs-12 col-sm-4 q-pa-sm">
              <q-card style="height: 100%"  class=" bg-secondary q-pa-sm" flat square>
                <q-card-section>
                  <div class="text-subtitle2">Januar 2010 - Februar 2016</div>
                  <div class="text-h6 q-pt-sm text-primary text-block-bold">Monday Consulting GmbH</div>

                </q-card-section>

                <q-card-section class="q-pt-none">
                  Als Software-Entwicklerin, Projektleiterin und Scrum Master war ich in mehreren Kundenprojekten tätig.
                  Ich konzipierte und entwickelte Applikationen, erstellte Projektpläne, überwachte den Projektfortschritt und entwickelte Wireframes.
                </q-card-section>
              </q-card>
            </div>
            <div class="col-xs-12 col-sm-4 q-pa-sm">
              <q-card style="height: 100%"  class="bg-secondary q-pa-sm" flat square>
                <q-card-section>
                  <div class="text-subtitle2">Mai 2007 - Dezember 2009</div>
                  <div class="text-h6 q-pt-sm text-primary text-block-bold">Capgemini sd&m</div>

                </q-card-section>

                <q-card-section class="q-pt-none">
                  In verschiedenen Projekten war ich für die Konzeption und Implementierung von kundenindividuellen
                  IT-Lösungen verantwortlich. In einigen Projekten übernahm ich die fachliche Führung der Projektmitarbeiter.
                </q-card-section>
              </q-card>
            </div>
          </div>
        </div>
      </div>

      <div class="col bg-primary" ref="me">

        <div class="row">
          <div class="col-12 col-sm-6 bg-office-image" style="min-height: 400px">
          </div>
          <div class="col-12 col-sm-6 q-pa-xl">
            <div class="column justify-center text-white" style="min-height: 300px">
              <div class="col-8 text-h3 q-pa-md">Über mich</div>
              <div class="col-8 text-h6 q-pa-md">Kurzprofil</div>
              <div class="col-8 q-pa-md">
                Im Bereich der Konzeptionierung und Entwicklung komplexer Softwarelösungen für verschiedenste Branchen
                habe ich in mehr als 15 Jahren vielfältige Erfahrung gesammelt. Ich verfüge über sehr starke
                analytische Fähigkeiten in Kombination mit einer strukturierten und ergebnisorientierten Herangehensweise.
                Mein hervorragendes Gespür für die Wünsche und Zielsetzungen der Kunden und mein hoher persönlicher
                Einsatz tragen wesentlich zum Erfolg der Projekte bei.
              </div>
            </div>
          </div>
        </div>

      </div>

      <div class="col bg-secondary" ref="projects">

        <div class="bg-white q-pa-lg-lg q-pa-sm-sm q-pa-md-md q-pa-xs-md text-center text-block-bold text-block-headline text-primary ">Projekte</div>

        <q-carousel
          v-model="slide"
          transition-prev="slide-right"
          transition-next="slide-left"
          swipeable
          animated
          control-color="primary"
          navigation
          padding
          infinite
          arrows
          height="530px"
          class="bg-secondary text-primary flat"
        >
          <q-carousel-slide name="prices" >
            <SoftwareProject
              title=" Neuentwicklung von Services im Bereich Preise"
              sector="Handel"
              methods="Kanban, Scrum, Microservices, Continuous Delivery"
              technologies="AWS, Spring Boot, Kotlin, React, Kafka, GitHub "
              short-description="Entwicklung verschiedener Microservices, zum Beispiel zur Berechnung von rechtskonformen Streichpreisen."
              description="Im Rahmen einer auf Microservices basierten Architektur wurden Backend-Anwendungen und eine Frontend Applikation in der AWS-Cloud umgesetzt. Ich konzipierte, entwickelte und testete Backend- und Frontend-Funktionalitäten."
              imageSrc="prices.jpg"
              imageStyle="width: 430px"
            />
          </q-carousel-slide>

          <q-carousel-slide name="tenant" >
            <SoftwareProject
              title=" Neuentwicklung eines „Mieter-Ökosystems“"
              sector="Finanzen"
              methods="Scrum, DDD, Microservices"
              technologies="AWS, Spring Boot, Kotlin, Vue.js "
              short-description="Entwicklung einer Plattform, die verschiedene Nutzungsaspekte kommerzieller Gebäude für den Nutzer bündelt."
              description="Im Rahmen einer auf Microservices basierten Architektur wurden eine App, ein Back-Office-System und
                    Backend-Anwendungen in der AWS-Cloud umgesetzt. Ich entwickelte vor allem Backend- Funktionalitäten,
                    aber half auch im Frontend aus. Ich erstellte Unit- und Integrationstests."
              imageSrc="parking.jpg"
              imageStyle="width: 230px"
            />
          </q-carousel-slide>

          <q-carousel-slide name="valuation" >
            <SoftwareProject
              title="Neuentwicklung einer Immobilienbewertung"
              sector="Immobilien"
              methods="Scrum, DDD, Microservices"
              technologies="Vue.js, Quasar, Java 11, Spring Boot "
              short-description="Entwicklung einer Immobilienbewertungsstrecke, Backend-Anwendungen und einem Back-Office-System
                    im Rahmen der Anwendungsdomäne Eigentümerkontakte."
              description="In einem agilen crossfunktionalen Team wurden diverse Microservices entwickelt. Ich übernahm in dem
                    Projekt sowohl Backend- als auch Frontend-Entwicklungen und erstellte Tests.
                    Eine teameigene Continuous Delivery Pipeline wurde aufgebaut und betreut."
              imageSrc="valuation.jpg"
              imageStyle="width: 360px"
            />
          </q-carousel-slide>

          <q-carousel-slide name="realestate" >
            <SoftwareProject
              title="Neuentwicklung einer Startseite eines Immobilienportals"
              sector="Immobilien"
              methods="Scrum, Schichtenarchitektur, Microservices"
              technologies="Java 8, Thymeleaf, Spring Boot, Gradle, Jenkins, Apache Mesos, DC/OS "
              short-description="Entwicklung von Microservices und einer Continuous Delivery Pipeline."
              description="Altsysteme wurden durch eine Microservice basierte Architektur abgelöst. Ich entwickelte
                    Backend- und Frontend- Funktionalitäten und half bei der Erstellung einer Continuous Delivery Pipeline."
              imageSrc="realestate.jpg"
              imageStyle="width: 320px"
            />
          </q-carousel-slide>

          <q-carousel-slide name="warehouse" >
            <SoftwareProject
              title="Neuentwicklung eines internationalen Portals zur Abwicklung warenwirtschaftlicher Prozesse"
              sector="Handel"
              methods="Agile Softwareentwicklung, Schichtenarchitektur"
              technologies="Java, JUnit, Spring Boot, SAP Java Connector, JDBC, Maven "
              short-description="Projektleitung, Konzeptionierung und Entwicklung einer Webanwendung zur Bereitstellung der
                     Warenwirtschaftsprozesse in den Filialen mit direktem Zugriff auf das zentrale SAP-System."
              description=""
              imageSrc="warehouse.jpg"
              imageStyle="width: 250px"
            />
          </q-carousel-slide>

          <q-carousel-slide name="stocktaking" >
            <SoftwareProject
              title="Entwicklung eines webbasierten Inventursystems"
              sector="Handel"
              methods="Agile Softwareentwicklung, Schichtenarchitektur"
              technologies="Java, Spring, Sencha Touch 2, CoreMedia 5.2 "
              short-description="Konzeptionierung und Entwicklung eines webgestützten Systems zur Inventurdurchführung für eine Einzelhandelskette. Sowohl Mobile- als auch Desktop-Variante."
              description=""
              imageSrc="stocktaking.jpg"
              imageStyle="width: 250px"
            />
          </q-carousel-slide>

          <q-carousel-slide name="planning" >
            <SoftwareProject
              title="Planungssystem"
              sector="Handel"
              methods="Iterative Softwareentwicklung"
              technologies="C#, Microsoft Visual Studio, MS SQL Server 2005 "
              short-description="Neuentwicklung und Konzeptionierung eines Planungssystems für den Non-Food-Bereich eines Handelshauses."
              description=""
              imageSrc="planing.jpg"
              imageStyle="width: 350px"
            />
          </q-carousel-slide>

        </q-carousel>

      </div>

      <div class="col bg-primary" style="min-height: 400px" ref="hobby">
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

      <div class="col bg-secondary text-primary" style="min-height: 100px">
        <div class="q-pa-lg row justify-center" ref="contact">
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
            <q-btn type="a" round color="primary"  href="https://www.linkedin.com/in/katrin-mischok" target="_blank">
            <q-avatar size="42px">
              <img src="~assets/linked-in.png">
            </q-avatar>
            </q-btn>
          </div>
        </div>
      </div>

      <div class="col bg-white text-primary" style="min-height: 325px">
        <div class="row q-pa-xl">
          <div class="col-xs-12 q-pa-sm text-center">
            <q-icon name="format_quote" style="font-size: 64px;"/>
          </div>
          <div class="col-xs-12 q-pa-sm text-center">
            <div class="text-h5 q-pa-md">"Well done is better than well said."</div>
          </div>
          <div class="col-xs-12 q-pa-sm text-center">
            <div class="text-subtitle q-pa-md">Benjamin Franklin</div>
          </div>
        </div>
      </div>
  </q-page>
</template>

<script>


import SoftwareProject from '../components/SoftwareProject';

export default {
  name: 'PageIndex',
  components: { SoftwareProject },
  data () {
    return {
      slide: 'stocktaking',
      name: null,
      email: null,
      subject: null,
      text: null,
      sm: ''
    }
  },
  methods: {
    mail () {
      window.location.href = 'mailto:info@katrinmischok.de?subject=Kontaktanfrage&body=Hallo%20Katrin,'
    },
    scrollToContact () {
      this.$refs.contact.scrollIntoView({ behavior: 'smooth' })
    },
    scrollToJobs () {
      this.$refs.jobs.scrollIntoView({ behavior: 'smooth' })
    },
    scrollToMe () {
      this.$refs.me.scrollIntoView({ behavior: 'smooth' })
    },
    scrollToProjects () {
      this.$refs.projects.scrollIntoView({ behavior: 'smooth' })
    },
    scrollToHobby () {
      this.$refs.hobby.scrollIntoView({ behavior: 'smooth' })
    }
  }
}
</script>
<style>
.bg-office-image {
  background-image: url(~assets/hamburg-office.jpg);
  background-repeat: no-repeat;
  background-size: cover;
  background-position-y: center;
}


.text-block-headline {
  font-size: 40px;
}

.text-block-bold {
  font-weight: 700;
}

.absolute-full, .fullscreen, .fixed-full {
  bottom: auto;
}
</style>
