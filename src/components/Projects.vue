<template>
  <div id="projects" class="projects">
    <div class="projects-heading heading">PREVIOUS PROJECTS</div>
    <transition-group name="projects-list" tag="div" class="projects-list">
      <div
        v-for="(project, index) in projects"
        :key="project"
        class="projects-list-item"
        :class="`projects-list-item-${index}`"
        v-on:click="rearrange(project, index)"
      >
        <div
          class="projects-list-item__image"
          :class="`projects-list-item__image-${project.id}`"
        >
          <div class="projects-list-item__image-name">
            {{ project.name }}
          </div>
          <!-- <img :src="project.src" :alt="project.src"> -->
        </div>
        <div v-if="index == 0" class="projects-list-item__description">
          <div class="projects-list-item__description-tagline">
            {{ project.tagline }}
          </div>
          <div class="projects-list-item__description-dialog">
            {{ project.description }}
          </div>
          <div class="projects-list-item__description-buffer"></div>
        </div>
      </div>
    </transition-group>

    <div class="projects-image"></div>
  </div>
</template>

<script>
export default {
  name: "Projects",
  data() {
    return {
      projects: [
        {
          id: "A",
          name: "Convene",
          tagline: "An awesome new way to meet",
          description: `Convene, at it's core is a cross platform tool to allow two people to find the best places to meet. Technically however, 
          it posed is significant and interesting challenge, needing to efficiently call and evaluate responses from several third party APIs. 
          It was built on a microservices architecture to more easily accomodate its cross platform nature. Frontend web app was built using VueJs,
          the mobile apps with Flutter and the cloud backend in NodeJs all hosted in Google Cloud Platform`,
        },
        {
          id: "B",
          name: "Motiv Box",
          tagline: "A new you in a box!",
          description: `The precursor to Made by Motiv limited. The company looked to overcome a glaring catch 22 in fitness - motivation is fleeting, how does one get
          themselves motivated to live a healthy lifestyle if they are not motivated to begin with. Getting fit takes a long time and sometimes
          we need a booster, something to break through the monotony and get us excited with our journey. To do this customers would sign up when
          they have an inital burst of motivation and every month there after get delivered a box of fitness clothing and equipment. The site was built on 
          a serverless stack with a vue front end and integrated stripe for payment methods and firebase authentication.`,
        },
        {
          id: "C",
          name: "The professional's guide to staying fit!",
          tagline: "How you can stay healthy depite a desk job",
          description: `This guide is not only for, but written by people who spend more that 40 hours a week
            behind a desk. Most personal trainers are on their feet all day, how can you be sure that their methods
            will work for you without that luxury? This guide breaks down that boundary, the authors are the proof.
            Priority is put on mental and physical health and hoped to educate the reader, so the principals can be
            used long into the future.`,
        },
      ],
    };
  },
  methods: {
    rearrange(project, index) {
      this.projects.splice(index, 1);
      this.projects.unshift(project);
    },
  },
};
</script>

<style lang="scss" scoped>
.projects {
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: $color-white;
  color: $color-text;
  font-family: $font-sans-sherif;
  padding: 3rem 0;
  font-size: $font-size-s;

  &-image{
    width: 100%;
    height: 120px;
    background-position: center;
    background-repeat: no-repeat;
    background-image: url(../assets/imgs/clickToSeeMore.png);
  }
}

.projects-list-move {
  transition: transform 0.5s ease-in-out;
}

.projects-list {
  // max-width: $size-app-max-width;
  display: grid;
  margin: 1rem;
  width: 100%;
  justify-content: center;
  grid:
    [row1-start] "second first " 20rem [row1-end]
    [row2-start] "third first " 20rem [row2-end]
    / 50% 50%;

  @media only screen and (max-width: $medium-breakpoint) {
    flex-direction: row;
    display: flex;
    flex-direction: column;
  }

  &-item {
    $root: &;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    opacity: 0.5;
    color: white;
    font-size: large;

    &:hover {
      opacity: 1;
      cursor: pointer;
    }
    &-0 {
      z-index: 10;
      grid-area: first;
      box-shadow: -4px 4px 16px -8px rgba(0, 0, 0, 0.85);
      opacity: 1;

      #{$root}__image{
          height: 20rem;
      }

    }
    &-1 {
      grid-area: second;
    }
    &-2 {
      grid-area: third;
    }

    &__description {
      background-color: white;
      height: 50%;
      color: $color-text;
      display: flex;
      flex-direction: column;
      
    justify-content: space-evenly;
      &-tagline {
        padding: 1rem;
        font-style: italic;
      }
      &-dialog {
        padding: 1rem;
      }
    }

    &__image {
      max-height: 20rem;
      height: 100%;
      width: 100%;
      background-position: center;
      background-size: cover;
      display: flex;
      align-items: flex-end;

      font-size: x-large;

      &-name {
        padding: 1rem;
        background: linear-gradient(
          0deg,
          rgba(41, 37, 44, 1) 0%,
          rgba(41, 37, 44, 0) 100%
        );
        width: 100%;
      }

      &-A {
        background-image: url(../assets/imgs/ConveneWeb.png);
      }
      &-B {
        background-image: url(../assets/imgs/MadeByMotivScreenshot.png);
      }
      &-C {
        background-image: url(../assets/imgs/MJPT.png);
      }
    }
  }
}
</style>