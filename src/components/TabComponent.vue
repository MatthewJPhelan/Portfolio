<template>
    <div class="tab-component">
        <div class="tab-component-company">{{ job.role }} <span>@ {{ job.company }}</span></div>
        <div class="tab-component-dates">{{ job.dates }}</div>
        <div
          class="tab-component-bulletpoint"
          v-for="bulletpoint in job.bulletpoints"
          :key="bulletpoint"
        >
          <span>></span> {{ bulletpoint }}
        </div>
    </div>
</template>

<script>
    export default {
        name: "TabComponent",
        props: {
            job: {
                type: Object,
                required: true,
            }
        }
    }
</script>

<style lang="scss" scoped>
.tab-component {
    min-width: 260px;
    background-color: $color-text;
    color: $color-white;
    padding: 0 1rem;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    border-radius: 0 $border-radius $border-radius 0;

    &-company {
        font-family: 'Quicksand';
        font-size: x-large;
        margin-bottom: 1rem;
        & span {
            color: $color-secondary;
        }
    }

    &-dates {
        font-family: 'Quicksand';
        font-size: large;
    }

    &-bulletpoint {
        font-family: 'Quicksand';
        font-size: large;
        padding-top: 1rem;

        & span {
            color: $color-highlight;
        }
    }
}
</style>