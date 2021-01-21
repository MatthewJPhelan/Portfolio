<template>
  <section class="footer" id="contact">
    <div class="footer-headshot"></div>
    <div class="footer-thanks">Thank you for visiting my website!</div>
    <div class="footer-text">
      If you wish to get in contact with me, LinkedIn or Email are best.
      <p>
        OR
        <a href="../assets/CV-2021.pdf" download>here</a
        >
        is my cv
      </p>
    </div>
    <Socials />
    <div class="footer-copyright">
      &copy; Matty J. Phelan {{ new Date().getFullYear() }}
    </div>
  </section>
</template>

<script>
import Socials from "./Socials.vue";
export default {
  name: "Footer",
  components: {
    Socials,
  },
};
</script>

<style lang="scss" scoped>
.footer {
  width: 100%;
  background-color: $color-white;
  display: flex;
  flex-direction: column;
  align-items: center;
  font-family: $font-sans-sherif;
  font-size: x-large;

  &-headshot {
    margin: 3rem;
    height: 20rem;
    width: 20rem;
    background-image: url(../assets/imgs/HeadShot.png);
    background-position: center;
    background-size: cover;
  }

  &-text {
    text-align: center;
  }

  &-copyright {
    font-size: small;
    padding-bottom: 1rem;
  }
}
</style>