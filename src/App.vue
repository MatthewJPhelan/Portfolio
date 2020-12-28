<template>
  <div class="app">
    <NavBar />
    <HeaderText />
    <Brands />
    <SectionTitle title="Previous Work" />
    <SplitSection
      title="title"
      tagLine="tagline"
      description="this is the description"
      imageLocation="../assets/imgs/MotivLogo.png"
    >
      <!-- <template v-slot:split-section-image>
        <img class="split-section-card__image" src=".\assets\imgs\MotivLogo.png" alt="" />
      </template> -->
    </SplitSection>
    <SplitSection
      title="title"
      tagLine="tagline"
      description="this is the description"
      imageLocation="src/imgs/MotivLogo.png"
    >
      <!-- <template v-slot:split-section-image>
        <img class="split-section-card__image" src=".\assets\imgs\ConveneLogo.png" alt="" />
      </template> -->
    </SplitSection>
    <Footer />
  </div>
</template>
<script lang="ts">
import { defineComponent } from "vue";
import NavBar from "@/components/NavBar.vue";
import HeaderText from "@/components/HeaderText.vue";
import Brands from "@/components/Brands.vue";
import SectionTitle from "@/components/SectionTitle.vue";
import SplitSection from "@/components/SplitSection.vue";
import Footer from "@/components/Footer.vue";

export default defineComponent({
  name: "App",
  components: {
    NavBar,
    HeaderText,
    Brands,
    SectionTitle,
    SplitSection,
    Footer,
  },
});
</script>

<style lang="scss">
.app {
  display: flex;
  flex-direction: column;
  margin: 3rem 2rem 0 2rem;
  max-width: $size-app-max-width;

  @media screen and (min-width: $medium-breakpoint) {
    margin: 3rem 3rem 0 3rem;
  }
  @media screen and (min-width: $large-breakpoint) {
    margin: 3rem 3rem 0 4rem;
  }
  @media screen and (min-width: $x-large-breakpoint) {
    margin: 3rem auto;
  }
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
