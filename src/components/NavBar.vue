<template>
  <section class="nav-bar">
    <div class="nav-bar-container">
      MATTY J. PHELAN
    </div>
  </section>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style lang="scss" scoped>
.nav-bar {
  width: 100%;
  padding: 1rem;
  background-color: $color-white;
  position: fixed;
  z-index: 99;
  box-shadow: 0px 8px 22px -10px rgba(0,0,0,0.6);

  &-container {
    font-family: $font-sans-sherif;
    font-size: $font-size-m;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 50px;
    text-align: center;
  }
}
</style>