<template>
  <div class="menu" @mouseleave="active = false">
    <a @click="change" class="burger" :class="active ? 'change' : ''">
      <div class="bar1"></div>
      <div class="bar2"></div>
      <div class="bar3"></div>
    </a>
    <ul class="menu-dropdown" @click="change" :class="active ? 'change' : ''">
      <li>
        <a href="#about">About</a>
      </li>
      <li>
        <a href="#experience">Experience</a>
      </li>
      <li>
        <a href="#skills">Skills</a>
      </li>
      <li>
        <a href="#projects">Projects</a>
      </li>
      <li>
        <a href="#ec">Extra Curricular</a>
      </li>
      <li>
        <a href="#contact">Contact</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Menu",
  data() {
    return {
      active: false,
    };
  },
  methods: {
    change() {
      this.active = !this.active;
    },
  },
};
</script>

<style lang="scss" scoped>
.menu {
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  width: 15rem;
  position: fixed;
  z-index: 99;
  right: 0;
  top: 1.5rem;
  cursor: pointer;
  font-family: $font-sans-sherif;
  font-size: $font-size-m;

  &-dropdown {
    box-shadow: -8px 16px 22px -10px rgba(0, 0, 0, 0.6);
    display: none;

    &.change {
      display: block;
      background-color: $color-white;
      padding: 3rem 2rem 1rem 2rem;
    }

    & li {
      margin-bottom: 1rem;
    }
  }
}
.burger {
  padding-right: 1rem;
}
.bar1,
.bar2,
.bar3 {
  width: 35px;
  height: 0.25rem;
  border-radius: 2px;
  background-color: $color-primary;
  margin: 6px 0;
  transition: 0.4s;
}

.change .bar1 {
  transform: rotate(-45deg) translate(-7px, 6px);
}

.change .bar2 {
  opacity: 0;
}

.change .bar3 {
  transform: rotate(45deg) translate(-7px, -8px);
}
</style>