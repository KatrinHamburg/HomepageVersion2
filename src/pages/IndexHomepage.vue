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

        <div class="q-pa-lg q-pt-xl text-center text-block-bold text-block-headline text-primary ">Projekte</div>

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
          height="500px"
          class="bg-secondary text-primary flat"
        >
          <q-carousel-slide name="prices" >
            <div class="column justify-center">
              <div class="row">

                <div class="col-12 col-md-6 q-pa-xs-xs q-pa-sm-sm q-pa-md-md q-pa-lg-lg q-pa-xl-xl">
                  <div class="text-h6">
                    Neuentwicklung von Services im Bereich Preise<br/>
                  </div>

                  <div class="text-subtitle2 q-pt-md">
                    Branche: Handel
                  </div>

                  <div class="text-subtitle2 q-pt-sm">
                    Methodiken: Kanban, Scrum, Microservices, Continuous Delivery
                  </div>

                  <div class="text-subtitle2 q-pt-sm">
                    Technologien: AWS, Spring Boot, Kotlin, React, Kafka, GitHub<br/>
                  </div>

                  <div class="q-pt-md">
                    Entwicklung verschiedener Microservices, zum Beispiel zur Berechnung von rechtskonformen Streichpreisen.
                  </div>

                  <div class="q-pt-md">
                    Im Rahmen einer auf Microservices basierten Architektur wurden Backend-Anwendungen und eine Frontend Applikation
                    in der AWS-Cloud umgesetzt. Ich konzipierte, entwickelte und testete Backend- und Frontend-Funktionalitäten.
                  </div>

                </div>
                <div class="gt-sm col-md-6 q-pa-lg text-center">
                  <q-img src="~assets/prices.jpg" style="width: 430px" />
                </div>
              </div>
            </div>
          </q-carousel-slide>

          <q-carousel-slide name="tenant" >
            <div class="column justify-center">
              <div class="row">

                <div class="col-12 col-md-6 q-pa-xs-xs q-pa-sm-sm q-pa-md-md q-pa-lg-lg q-pa-xl-xl">
                  <div class="text-h6">
                    Neuentwicklung eines „Mieter-Ökosystems“<br/>
                  </div>

                  <div class="text-subtitle2 q-pt-md">
                    Branche: Finanzen
                  </div>

                  <div class="text-subtitle2 q-pt-sm">
                    Methodiken: Scrum, DDD, Microservices
                  </div>

                  <div class="text-subtitle2 q-pt-sm">
                    Technologien: AWS, Spring Boot, Kotlin, Vue.js <br/>
                  </div>

                  <div class="q-pt-md">
                    Entwicklung einer Plattform, die verschiedene Nutzungsaspekte kommerzieller Gebäude für den Nutzer bündelt.
                  </div>

                  <div class="q-pt-md">
                    Im Rahmen einer auf Microservices basierten Architektur wurden eine App, ein Back-Office-System und
                    Backend-Anwendungen in der AWS-Cloud umgesetzt. Ich entwickelte vor allem Backend- Funktionalitäten,
                    aber half auch im Frontend aus. Ich erstellte Unit- und Integrationstests. In dem Projekt galt
                    ich als die Domänen-Expertin.
                  </div>


                </div>
                <div class="gt-sm col-md-6 q-pa-lg text-center">
                  <q-img src="~assets/parking.jpg" style="width: 300px" />
                </div>
              </div>
            </div>
          </q-carousel-slide>


          <q-carousel-slide name="valuation" >
            <div class="column justify-center">
              <div class="row">

                <div class="col-12 col-md-6 q-pa-xs-xs q-pa-sm-sm q-pa-md-md q-pa-lg-lg q-pa-xl-xl">
                  <div class="text-h6">
                    Neuentwicklung einer Immobilienbewertung<br/>
                  </div>

                  <div class="text-subtitle2 q-pt-md">
                    Branche: Immobilien
                  </div>

                  <div class="text-subtitle2 q-pt-sm">
                    Methodiken: Scrum, DDD, Microservices, Continuous Delivery
                  </div>

                  <div class="text-subtitle2 q-pt-sm">
                    Technologien: Vue.js, Quasar, Java 11, Spring Boot <br/>
                  </div>

                  <div class="q-pt-md">
                    Entwicklung einer Immobilienbewertungsstrecke, Backend-Anwendungen und einem Back-Office-System
                    im Rahmen der Anwendungsdomäne Eigentümerkontakte
                  </div>

                  <div class="q-pt-md">
                  In einem agilen crossfunktionalen Team wurden diverse Microservices entwickelt. Ich übernahm in dem
                    Projekt sowohl Backend- als auch Frontend-Entwicklungen und erstellte Tests.
                    Eine teameigene Continuous Delivery Pipeline wurde aufgebaut und betreut.
                  </div>


                </div>
                <div class="gt-sm col-md-6 q-pa-lg text-center">
                  <q-img src="~assets/valuation.jpg" style="width: 400px" />
                </div>
              </div>
            </div>
          </q-carousel-slide>
          <q-carousel-slide name="realestate" >
            <div class="column justify-center">
              <div class="row">

                <div class="col-12 col-md-6 q-pa-xs-xs q-pa-sm-sm q-pa-md-md q-pa-lg-lg q-pa-xl-xl ">
                  <div class="text-h6">
                    Neuentwicklung einer Startseite eines Immobilienportals als Microservice Architektur<br/>
                  </div>

                  <div class="text-subtitle2 q-pt-md">
                    Branche: Immobilien
                  </div>

                  <div class="text-subtitle2 q-pt-sm">
                    Methodiken: Scrum, Schichtenarchitektur, Microservices<br/>
                  </div>

                  <div class="text-subtitle2 q-pt-sm">
                    Technologien: Java 8, Thymeleaf, Spring Boot, Gradle, Jenkins, Apache Mesos, DC/OS <br/>
                  </div>

                  <div class="q-pt-md">
                    Entwicklung von Microservices und einer Continuous Delivery Pipeline
                  </div>

                  <div class="q-pt-md">
                  Altsysteme wurden durch eine Microservice basierte Architektur abgelöst. Ich entwickelte
                    Backend- und Frontend- Funktionalitäten und half bei der Erstellung einer Continuous Delivery Pipeline.
                  </div>

                </div>
                <div class="gt-sm col-md-6 q-pa-xl text-center">
                  <q-img src="~assets/realestate.jpg" style="width: 400px" />
                </div>
              </div>
            </div>
          </q-carousel-slide>
          <q-carousel-slide name="warehouse" >
            <div class="column justify-center">
              <div class="row">

                <div class="col-12 col-md-6 q-pa-xs-xs q-pa-sm-sm q-pa-md-md q-pa-lg-lg q-pa-xl-xl ">
                  <div class="text-h6">
                  Neuentwicklung eines internationalen Portals zur Abwicklung warenwirtschaftlicher Prozesse <br/>
                    </div>

                  <div class="text-subtitle2 q-pt-md">
                    Branche: Handel
                  </div>

                  <div class="text-subtitle2 q-pt-sm">
                    Methodiken: Agile Softwareentwicklung, Schichtenarchitektur
                  </div>

                  <div class="text-subtitle2 q-pt-sm">
                    Technologien: Java, JUnit, Spring Boot, SAP Java Connector, JDBC, Maven <br/>
                  </div>

                   <div class="q-pt-md">
                  Projektleitung, Konzeptionierung und Entwicklung einer Webanwendung zur Bereitstellung der
                     Warenwirtschaftsprozesse in den Filialen mit direktem Zugriff auf das zentrale SAP-System. <br/>
                  </div>

                </div>
                <div class="gt-sm col-md-6 q-pa-xl text-center">
                  <q-img src="~assets/warehouse.jpg" style="width: 450px" />

                </div>
              </div>
            </div>
          </q-carousel-slide>
          <q-carousel-slide name="stocktaking" >
            <div class="column justify-center">
              <div class="row">

                <div class="col-12 col-md-6 q-pa-xs-xs q-pa-sm-sm q-pa-md-md q-pa-lg-lg q-pa-xl-xl ">
                  <div class="text-h6">
                    Entwicklung eines webbasierten Inventursystems <br/>
                  </div>

                  <div class="text-subtitle2 q-pt-md">
                    Branche: Handel
                  </div>

                  <div class="text-subtitle2 q-pt-sm">
                    Technologien: Java, Spring, Sencha Touch 2, CoreMedia 5.2<br/>
                  </div>

                  <div class="q-pt-md">
                    Konzeptionierung und Entwicklung eines webgestützten Systems zur Inventurdurchführung für eine Einzelhandelskette. Sowohl Mobile- als auch Desktop-Variante.<br/>
                  </div>

                </div>
                <div class="gt-sm col-md-6 q-pa-xl text-center">
                  <q-img src="~assets/stocktaking.jpg" style="width: 450px" />
                </div>
              </div>
            </div>
          </q-carousel-slide>
          <q-carousel-slide name="planning" >
            <div class="column justify-center">
              <div class="row">

                <div class="col-12 col-md-6 q-pa-xs-xs q-pa-sm-sm q-pa-md-md q-pa-lg-lg q-pa-xl-xl ">
                  <div class="text-h6">
                    Planungssystem <br/>
                  </div>

                  <div class="text-subtitle2 q-pt-md">
                    Branche: Handel
                  </div>

                  <div class="text-subtitle2 q-pt-xs">
                    Technologien: C#, Microsoft Visual Studio, MS SQL Server 2005<br/>
                  </div>

                  <div class="q-pt-md">
                    Neuentwicklung und Konzeptionierung eines Planungssystems für den Non-Food-Bereich eines Handelshauses.<br/>
                  </div>

                </div>
                <div class="gt-sm col-md-6 q-pa-xl text-center">
                  <q-img src="~assets/planing.jpg" style="width: 450px" />
                </div>
              </div>
            </div>
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
export default {
  name: 'PageIndex',
  data () {
    return {
      lorem: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
      slide: 'prices',
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
