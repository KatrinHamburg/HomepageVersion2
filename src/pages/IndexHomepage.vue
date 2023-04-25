<template>
  <q-page class="bg-white">

    <HeadArea
      :scroll-to-contact="scrollToContact"
      :scroll-to-hobby="scrollToHobby"
      :scroll-to-jobs="scrollToJobs"
      :scroll-to-me="scrollToMe"
      :scroll-to-projects="scrollToProjects" />

    <div ref="jobs">
      <WorkExperience />
    </div>

    <div ref="me">
      <AboutMe />
    </div>

    <div ref="projects">
      <ProjectCarousel />
    </div>

    <div ref="hobby">
      <HobbyArea />
    </div>

    <div ref="contact">
      <ContactMe :mail="mail" :sm="sm" />
    </div>

    <QuoteArea />
  </q-page>
</template>

<script>


import WorkExperience from "./subpages/WorkExperience";
import AboutMe from "./subpages/AboutMe";
import ProjectCarousel from "./subpages/ProjectCarousel";
import HobbyArea from "./subpages/HobbyArea";
import ContactMe from "./subpages/ContactMe";
import QuoteArea from "./subpages/QuoteArea";
import HeadArea from "./subpages/HeadArea";

export default {
  name: "PageIndex",
  components: { HeadArea, QuoteArea, ContactMe, HobbyArea, ProjectCarousel, AboutMe, WorkExperience },
  data() {
    return {
      name: null,
      email: null,
      subject: null,
      text: null,
      sm: ""
    };
  },
  methods: {
    mail() {
      window.location.href = "mailto:info@katrinmischok.de?subject=Kontaktanfrage&body=Hallo%20Katrin,";
    },
    scrollToContact() {
      this.$refs.contact.scrollIntoView({ behavior: "smooth" });
    },
    scrollToJobs() {
      this.$refs.jobs.scrollIntoView({ behavior: "smooth" });
    },
    scrollToMe() {
      this.$refs.me.scrollIntoView({ behavior: "smooth" });
    },
    scrollToProjects() {
      this.$refs.projects.scrollIntoView({ behavior: "smooth" });
    },
    scrollToHobby() {
      this.$refs.hobby.scrollIntoView({ behavior: "smooth" });
    }
  }
};
</script>
<style>
.absolute-full, .fullscreen, .fixed-full {
  bottom: auto;
}
</style>
