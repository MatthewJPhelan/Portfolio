<template>
    <div class="kanban-column">
        <div class="kanban-column__title">
        {{ title }}
        </div>
        <div class="kanban-column__skills">
            <div class="kanban-column__skills--skill" v-for="skill in skills" :key="skill">
                {{ skill }}
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "KanbanColumn",
        props: {
            title: {
                type: String,
                required: true,
            },
            skills: {
                type: Array,
                required: true,
            }
        }
    }
</script>

<style lang="scss" scoped>
.kanban-column {
    padding: 1rem;
    font-family: 'Permanent Marker', cursive;
    font-size: x-large;
    &__title {
        border-bottom: 2px solid $color-text;
        margin-bottom: 1rem;
        text-align: center;
    }

    &__skills {
        &--skill {
            display: flex;
            justify-content: center;
            align-items: center;
            width: 135px;
            height: 135px;
            font-size: large;
            text-align: center;

            background-image: url("../assets/imgs/stickyNote.png");
            background-position: center;
            background-size: contain;
        }
    }
}
</style>