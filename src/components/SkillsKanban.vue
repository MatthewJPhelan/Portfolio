<template>
  <div class="skills-kanban" id="skills">
    <div class="skills-kanban-heading heading">SKILLS KANBAN</div>
    <div class="skills-kanban-spotlights">
        <img src="../assets/imgs/spotlights.png" alt="">
    </div>
    <div class="skills-kanban-board">
      <div class="skills-kanban-board__collumns">
        <div class="skills-kanban-board__collumns--backlog">
          <KanbanColumn title="backlog" :skills="['React', 'Unity']" />
        </div>
        <div class="skills-kanban-board__collumns--in-progress">
          <KanbanColumn
            title="in-progress"
            :skills="['Flutter', 'Illustrator', 'Photoshop', 'XD']"
          />
        </div>
        <div class="skills-kanban-board__collumns--review">
          <KanbanColumn
            title="review"
            :skills="[
              'Sitecore',
              'Google Cloud Platform',
              'NodeJs',
              'Google Ad Platform',
            ]"
          />
        </div>
        <div class="skills-kanban-board__collumns--done">
          <KanbanColumn title="done" :skills="['VueJs', '.Net', 'Azure']" />
        </div>
      </div>
    </div>
    <div class="skills-kanban-logos">
        <div class="skills-kanban-logos__img">
            <img src="../assets/imgs/vuejs.png" alt="">
        </div>
        <div class="skills-kanban-logos__img">
            <img src="../assets/imgs/csharp.png" alt="">
        </div>
        <div class="skills-kanban-logos__img">
            <img src="../assets/imgs/sitecore.png" alt="">
        </div>
        <div class="skills-kanban-logos__img">
            <img src="../assets/imgs/azure.png" alt="">
        </div>
        <div class="skills-kanban-logos__img">
            <img src="../assets/imgs/gcp.png" alt="">
        </div>
    </div>
  </div>
</template>

<script>
import KanbanColumn from "./KanbanColumn.vue";
export default {
  name: "SkillsKanban",
  components: {
    KanbanColumn,
  },
};
</script>

<style lang="scss" scoped>
.skills-kanban {
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: $color-primary;
  color: $color-text;
  font-family: $font-sans-main;
  padding: 3rem 0;
  font-size: $font-size-s;
  
  &-heading {
      margin-bottom: 0;
      color: $color-white;
  }
    &-spotlights {
        height: 110px;
        width: 100%;
        overflow: hidden;
        display: flex;
        justify-content: center;
        & img {
            width: 1200px;
        }
    }
  &-board {
    background-color: white;
    box-shadow: 5px 5px 19px -1px rgba(63, 63, 63, 0.56);
    padding: 1rem;
    border-radius: 0.5rem;
    width: 90%;

    &__collumns {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-evenly;

      @media only screen and (max-width: $medium-breakpoint) {
        justify-content: center;
      }
    }
  }
  &-logos {
      margin-top: 2rem;
      display: flex;
      justify-content: space-evenly;
      flex-wrap: wrap;
      width: 100%;

      &__img {
          height: 4rem;
            margin: 0.5rem 2rem;
          & img{
              height: 100%;
          }
      }
  }
}
</style>