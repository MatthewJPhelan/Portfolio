<template>
  <section class="header-text">
    <div class="header-text-container">
      <div class="header-text-container--content">
        <div class="header-text-container--content__title">
          I work with <span class="highlighted-text">startups and top companies</span> to design inclusive, effective,
          and <span class="highlighted-text">impactful digital products.</span>
        </div>
        <div class="header-text-container--content__about">
          <Column
            title="Title"
            content="I'm Matt, a Full stack developer from London. I’ve been programming for over a 7 years."
          />
          <Column
            class="column-middle"
            title="Title"
            content="I'm Matt, a Full stack developer from London. I’ve been programming for over a 7 years."
          />
          <Column
            title="Title"
            content="I'm Matt, a Full stack developer from London. I’ve been programming for over a 7 years."
          />
        </div>
      </div>
      <Underline class="header-text-container-underline" />
    </div>
  </section>
</template>

<script>
import Underline from "@/assets/icons/Underline.vue";
import Column from "@/components/Column.vue";
export default {
  name: "HeaderText",
  components: {
    Underline,
    Column,
  },
};
</script>

<style lang="scss" scoped>
.header-text {
  &-container {
    &--content {
      &__title {
        max-width: 600px;
        padding-top: 20vh;
        margin: 4rem 0;
        font-size: xx-large;
        color: $color-primary;
      }
      &__about {
        display: flex;
        justify-content: left;
        align-items: flex-end;
        margin: 4rem 0;
        flex-direction: column;
        @media screen and (min-width: $medium-breakpoint) {
          flex-direction: row;
        }
      }
    }

    &-underline {
      max-width: 600px;
      margin: 4rem 0;
    }
  }
}
</style>