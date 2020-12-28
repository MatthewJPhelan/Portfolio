<template>
  <section class="footer">
    <FooterScribble class="footer-scribble" />
    this is the footer
  </section>
</template>

<script>
import FooterScribble from "@/assets/imgs/FooterScribble.vue";
export default {
  name: "Footer",
  components: {
    FooterScribble,
  },
};
</script>

<style lang="scss" scoped>
.footer {
  width: 100%;
  position: absolute;
  left: 0;
  bottom: -200vh;
  background-color: $color-primary;
  display: flex;
  flex-direction: column;
  justify-content: center;

  &-scribble {
    position: relative;
    top: -5px;
    left: 0;
    width: 100%;
    height: 100%;
  }
}
</style>