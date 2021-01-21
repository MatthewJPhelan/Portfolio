<template>
  <div class="extra-curricular" id="ec">
    <div class="extra-curricular-heading heading">Extra Curricular</div>
    <div class="extra-curricular-container">
      <div class="extra-curricular-container__card">
        <div
          class="extra-curricular-container__card--img PersonalTraining"
        ></div>
        <div
          class="extra-curricular-container__card--description"
        >
          Early 2020 I completed my level 3 personal training and nutrition certifications.
        </div>
      </div>
      <div class="extra-curricular-container__card">
        <div class="extra-curricular-container__card--img LPTrust"></div>
        <div
          class="extra-curricular-container__card--description"
        >
          After growing my hair for upwards of 18 months, in Mid 2020 I donated 10 inches of hair to the Little princess trust - a truly great cause.
        </div>
      </div>
      <div class="extra-curricular-container__card">
        <div class="extra-curricular-container__card--img Acapella"></div>
        <div
          class="extra-curricular-container__card--description"
        >
          I have always enjoyed singing, and in 2018 I had the great honor of performing with my university acapella group - the Trebles - at Edinburgh Fringe festival of the arts. 
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ExtraCurricular",
};
</script>

<style lang="scss" scoped>
.extra-curricular {
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: $color-highlight;
  color: $color-white;
  font-family: $font-sans-sherif;
  padding: 3rem 0;
  font-size: $font-size-s;

  &-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    &__card {
      margin: 1rem;
      background-color: $color-white;
      color: $color-text;
      font-size: large;
      min-height: 30rem;
      width: 20rem;
      border-radius: $border-radius;
      box-shadow: $box-shadow-standard;

      &--img {
        width: 100%;
        height: 20rem;
        background-color: $color-primary;
        background-position: center;
        background-size: cover;
        border-radius: $border-radius $border-radius 0 0;

        &.PersonalTraining {
          background-image: url(../assets/imgs/PersonalTraining.jpg);;
        }
        &.LPTrust {
          background-image: url(../assets/imgs/LPTrust.jpg);
        }
        &.Acapella {
          background-image: url(../assets/imgs/acapella.jpg);
          background-position: left;
        }
      }

      &--description {
        margin: 1rem;
      }
    }
  }
}
</style>