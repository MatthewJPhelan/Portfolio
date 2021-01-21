<template>
  <div id="experience" class="work-experience">
    <div class="work-experience-heading heading">WORK EXPERIENCE</div>
    <div class="work-experience-container">
      <div class="work-experience-container__tabs">
        <div
          class="work-experience-container__tabs-name"
          v-for="company in companies"
          :key="company"
          v-on:click="changeActiveTab(company)"
          :class="company == activeTab ? 'active' : ''"
        >
          {{ company }}
        </div>
      </div>
      <div
        class="work-experience-container__content"
        v-for="job in experience"
        :key="job.company"
        :class="job.company == activeTab ? 'active' : ''"
      >
        <TabComponent :job="job" v-if="job.company == activeTab" />
      </div>
    </div>
  </div>
</template>

<script>
import TabComponent from "./TabComponent.vue";
export default {
  name: "WorkExperience",
  components: {
    TabComponent,
  },
  data() {
    return {
      activeTab: "Valtech",
      companies: ["Made By Motiv", "Valtech", "MG OMD", "Nex Group", "NHS"],
      experience: [
        {
          company: "Made By Motiv",
          dates: "Jul 2020 - Present",
          role: "Founder",
          bulletpoints: [
            "Through my background in software engineering and personal training, I look to innovate in the fitness space and help create good habits.",
            "Using some of the most cutting edge web technologies I have built a cross platform applicaton that is responsive, intuitive and automatically scales to demand.",
            "The website at the company’s core is built on using Vuejs and the app is built in Flutter.",
            "Both utilise a microservices architecture with a nodejs backend and web api, both hosted in Google Cloud Platform",
          ],
        },
        {
          company: "Valtech",
          dates: "Jul 2019 - Aug 2020",
          role: "Full Stack Software Engineer",
          bulletpoints: [
            "Worked on multiple large scale projects for high profile clients including Taylor Wimpey, Bupa and Bennetts.",
            "Worked on a variety of different stories  through the full stack, using VueJs, C#, .Net, Sitecore and Azure.",
            "Took the lead in implementing new technologies into projects such as integrating Storybook with Vue and invision.",
            "Worked closely with a team both in person and remotely due to Covid-19, utilising software such as Slack, Microsoft Teams, Jira, Confluence and Miro.",
          ],
        },
        {
          company: "MG OMD",
          dates: "Dec 2018 - Jun 2019",
          role: "Advertising Operations Executive",
          bulletpoints: [
            "Worked closely with client teams to create, maintain and troubleshoot online advertisement serving using Google’s Advertising suite, Sizemek and Facebook’s ad manager.",
            "Maintained up-to-date knowledge of low level advertising infrastructure and consulted on best technology.",
            "Aided team efficiency of trafficking processes by developing web technologies in javascript to automate production and triage of advertising scripts.",
          ],
        },
        {
          company: "Nex Group",
          dates: "Dec 2017 - Jan 2018",
          role: "IT Intern",
          bulletpoints: [
            "Designed and implemented a production ready integrated Service-Now widget in company’s Outlook email window with HTML, CSS and JavaScript.",
            "The integration of the widget was taken through the full development lifecycle.",
            "It allowed users to open a ticket with the IT team in one click saving a huge amount of man hours.",
            "The widget was designed to be intuitive and easily usable encouraging end-users to engage.",
          ],
        },
        {
          company: "NHS",
          dates: "Jan 2014 - Apr 2014",
          role: "Retrospective Administrator",
          bulletpoints: [
            "Worked on a secure and complex application to aid traveling nurses increating and updating patient data and data reporting.",
            "The solution was event driven and written on a Visual Basic stack.",
            "It had an emphasis on clean user input, with validated forms throughout, saving the NHS hundreds of hours of administrative work every month on data clensing and reliable reporting.",
          ],
        },
      ],
    };
  },
  methods: {
    changeActiveTab(tabName) {
      this.activeTab = tabName;
    },
  },
};
</script>

<style lang="scss" scoped>
.work-experience {
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: $color-white;
  color: $color-text;
  font-family: $font-sans-main;
  padding: 3rem 0;
  font-size: $font-size-s;

  &-container {
    border-radius: 1rem;
    display: flex;
    width: 90%;
    box-shadow: $box-shadow-standard;

    @media only screen and (max-width: $small-breakpoint) {
      flex-direction: column;
      width: 100%;
    }

    &__tabs {
      display: flex;
      flex-direction: column;
      align-items: stretch;
      cursor: pointer;
      @media only screen and (max-width: $small-breakpoint) {
        flex-direction: row;
      }

      &-name {
        flex: 1;
        width: 90%;
        padding: 0.5rem;
        background-color: $color-white;
        font-family: "Quicksand";
        font-size: large;
      }

      & .active {
        color: red;
        box-shadow: $box-shadow-standard;
        z-index: 50;
      }
    }

    &__content {
      &.active {
        height: 440px;
        width: 100%;
      }
    }
  }
}
</style>