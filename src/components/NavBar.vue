<template>
  <section class="nav-bar">
    <div class="nav-bar-container">
      <img src="../assets/imgs/LogoWName.png" alt="Logo" />
      <div class="nav-bar-container__contact">
        <Contact />
      </div>
    </div>
  </section>
</template>

<script>
import Contact from "@/assets/icons/Contact";
export default {
  name: "Navbar",
  components: {
    Contact,
  },
};
</script>

<style lang="scss" scoped>
.nav-bar {
  width: 100%;
  margin-top: 2rem;
  &-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 50px;

    &__contact {
        height: 3rem;
        width: 3rem;
        background-color: $color-primary;
        border-radius: 8px;
        box-shadow: 4px 4px 16px -8px rgba(0,0,0,0.75);
        display: flex;
        justify-content: center;
      & svg {
        height: 100%;
      }
    }
  }
}
</style>