<template>
  <div class="about" id="about">
    <div class="about-heading heading">
      HELLO WORLD! I'M A FULL STACK DEVELOPER.
    </div>
    <div class="about-code">
      <div class="about-code__input">
        <div class="about-code__input--date">Last login: {{ date }}</div>
        <Terminal input="matty.location">=> {{ matty.origin }}</Terminal>
        <Terminal input="matty.coreSkills">=> {{ matty.coreSkills }}</Terminal>
        <Terminal input="matty.workExperience.last">
          <div v-for="line in matty.workExperience" :key="line">
            => {{ line }}
          </div>
        </Terminal>
        <Terminal input="matty.education">
          <div v-for="degree in matty.education" :key="degree.name">
            => {{ degree }}
          </div>
        </Terminal>
        <Terminal input="matty.interests">=> {{ matty.interests }}</Terminal>
        <Terminal input="matty.cv">
          => <a href="../assets/CV-2021.pdf" download>mattyjphelan.pdf</a>
        </Terminal>
        <Terminal input="matty.socialAccounts">
          <div>
            => LinkedIn:
            <a
              href="https://www.linkedin.com/in/matthew-j-phelan-1a9998108/"
              
              >matthewjphelan</a
            >
          </div>
          <div>
            => Github:
            <a href="https://github.com/MatthewJPhelan" 
              >matthewjphelan</a
            >
          </div>
          <div>
            => Instagram:
            <a href="https://www.instagram.com/mattyjphelan" 
              >@mattyjphelan</a
            >
          </div>
        </Terminal>
        <Terminal input="matty.emailAddress">
          =>
          <a href="mailto:matthew.phelanonline@gmail.com"
            >matthew.phelanonline@gmail.com</a
          >
        </Terminal>
        <div class="about-code__input--cursor">
          mattyjphelan ~ %
          <div class="about-code__input--cursor-block"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Terminal from "./Terminal.vue";
export default {
  name: "About",
  components: {
    Terminal,
  },
  data() {
    const todaysDate = new Date();
    return {
      date: todaysDate.toString(),
      matty: {
        origin: "London, UK",
        education: [
          {
            masters: {
              name: "MSc Computer Science",
              grade: "distinction",
              institution: "University of Birmingham",
            },
          },
          {
            undergrad: {
              name: "BSc Business Management",
              grade: "2:1",
              institution: "University of Birmingham",
            },
          },
        ],
        interests: "['Health', 'Music', 'Coffee', 'Cooking', 'Puzzles']",
        coreSkills:
          "['VueJs', '.Net', 'Sitecore', 'Azure', 'Google Cloud Platform']",
        workExperience: [
          "company: Valtech UK",
          "role: Full stack software engineer",
          "start_date: Jul 2019",
          "end_date: Aug 2020",
        ],
      },
    };
  },
};
</script>

<style lang="scss" scoped>
.about {
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: $color-highlight;
  color: $color-white;
  font-family: $font-sans-main;
  padding: 3rem 0;
  font-size: $font-size-s;

  &-code {
    background-color: $color-white;
    max-width: $size-app-max-width;
    min-width: 360px;
    padding-top: 0.5rem;
    border-radius: 5px 5px 0 0;

    &__input {
      background-color: $color-text;
      padding: 0.5rem;

      &--cursor {
        display: flex;
        &-block {
          width: 0.2rem;
          height: 0.75rem;
          background-color: white;
          margin-left: 0.25rem;
          animation: blink 1s infinite;
          @keyframes blink {
            0% {
              opacity: 0;
            }
            50% {
              opacity: 1;
            }
            100% {
              opacity: 0;
            }
          }
        }
      }
    }
  }
}
</style>