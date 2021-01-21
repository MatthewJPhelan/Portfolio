<template>
  <div class="socials">
    <div class="socials">
      <a class="socials__img" href="mailto:matthew.phelanonline@gmail.com">
        <img src="../assets/imgs/emailicon.png" alt="email icon" />
      </a>
      <a class="socials__img" href="https://www.linkedin.com/in/matthew-j-phelan-1a9998108/">
        <img src="../assets/imgs/liicon.png" alt="LinkedIn icon" />
      </a>
      <a class="socials__img" href="https://github.com/MatthewJPhelan">
        <img src="../assets/imgs/ghicon.png" alt="Github icon" />
      </a>
      <a class="socials__img" href="https://www.instagram.com/mattyjphelan">
        <img src="../assets/imgs/igicon.png" alt="Instagram icon" />
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "Socials",
};
</script>

<style lang="scss" scoped>
.socials {
  margin: 2rem 0;
  display: flex;
  justify-content: space-evenly;
  width: 260px;

  &__img {
    height: 2rem;

    & img {
      height: 100%;
    }
  }
}
</style>