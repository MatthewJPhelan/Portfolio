<template>
  <div class="app">
    <NavBar />
    <Menu />
    <Header />
    <About />
    <WorkExperience />
    <SkillsKanban />
    <Projects />
    <ExtraCurricular />
    <Footer />
  </div>
</template>
<script lang="ts">
import { defineComponent } from "vue";
import NavBar from "@/components/NavBar.vue";
import Menu from "@/components/Menu.vue"
import Header from "@/components/Header.vue"
import About from '@/components/About.vue';
import SkillsKanban from '@/components/SkillsKanban.vue';
import WorkExperience from '@/components/WorkExperience.vue';
import Projects from '@/components/Projects.vue';
import ExtraCurricular from '@/components/ExtraCurricular.vue'; 
import Footer from "@/components/Footer.vue";

export default defineComponent({
  name: "App",
  components: {
    NavBar,
    Menu,
    Header,
    About,
    SkillsKanban,
    WorkExperience,
    Projects,
    ExtraCurricular,
    Footer,
  },
});
</script>

<style lang="scss">
.app {
  display: flex;
  flex-direction: column;
  color: $color-text;
  // margin: 3rem 2rem 0 2rem;
  // max-width: $size-app-max-width;

  // @media screen and (min-width: $medium-breakpoint) {
  //   margin: 3rem 3rem 0 3rem;
  // }
  // @media screen and (min-width: $large-breakpoint) {
  //   margin: 3rem 3rem 0 4rem;
  // }
  // @media screen and (min-width: $x-large-breakpoint) {
  //   margin: 3rem auto;
  // }
  // &__content {
  //   max-width: $size-app-max-width;
  //   margin: auto;
  //   display: flex;
  //   flex-direction: column;
  //   padding-bottom: $grid-20;
  // }

  &__nav {
    flex: 0 0 $grid-40;
  }

  &__inner-content {
    padding: $grid-3 $grid-7;
    flex-grow: 1;
  }
}
</style>
