<template>
  <section class="brands">
    <!-- <h2 class="brands-title">Brands</h2> -->
    <div class="brands-logos">
      <img
        class="brands-logos-img"
        src="../assets/imgs/TaylorWimpeyLogo.png"
        alt="Taylor Wimpey Logo"
      />
      <img
        class="brands-logos-img"
        src="../assets/imgs/BupaLogo.png"
        alt="Taylor Wimpey Logo"
      />
      <img
        class="brands-logos-img"
        src="../assets/imgs/BennettsLogo.png"
        alt="Bennetts Logo"
      />
      <img
        class="brands-logos-img"
        src="../assets/imgs/ConveneLogo.png"
        alt="Convene Logo"
      />
      <img
        class="brands-logos-img"
        src="../assets/imgs/MotivLogo.png"
        alt="Motiv Logo"
      />
    </div>
    <Underline class="brands-underline" />
  </section>
</template>

<script>
import Underline from "@/assets/icons/Underline.vue";
export default {
  name: "Brands",
  components: {
    Underline,
  },
};
</script>

<style lang="scss" scoped>
.brands {
  display: flex;
  align-items: center;
  flex-direction: column;
  &-title {
    margin-top: 4rem;
    font-weight: 900;
    font-size: x-large;
  }

  &-logos {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: flex-start;
    margin: 4rem 0;
    &-img {
      margin: 2rem;
      max-width: 120px;
    }
  }

  &-underline {
    max-width: 600px;
    margin: 4rem 0;
    transform: scale(-1, 1);
    align-self: flex-end;
  }
}
</style>