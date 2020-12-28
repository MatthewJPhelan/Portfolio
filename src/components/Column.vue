<template>
  <div class="column">
    <!-- <div class="column-title">{{ title }}</div> -->
    <div class="column-content">{{ content }}</div>
  </div>
</template>

<script>
export default {
  name: "Column",
  props: {
    title: String,
    content: String,
  },
};
</script>

<style lang="scss" scoped>
.column {
    min-width: 200px;
    margin: 1rem 0;
    font-size: large;

  &-middle {
      @media screen and (min-width: $medium-breakpoint) {
        margin-left: 2rem;
        margin-right: 2rem;
      }
  }
}
</style>