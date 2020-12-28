<template>
    <div class="section-title">
        <h3 class="section-title-words">{{ title }}</h3>
        <div class="section-title-underline"></div>
    </div>
</template>

<script>
    export default {
        name: "SectionTitle",
        props: {
            title: String
        }
    }
</script>

<style lang="scss" scoped>
.section-title {
    $root: &;

    margin: 4rem auto;

    &:hover {
        #{$root}-underline {
            height: 2px;
            width: 8rem;
            background-color: $color-primary;
        }
    }

    &-underline {
        height: 2px;
        width: 4rem;
        margin: auto;
        background-color: $color-primary;
        transition: .5s ease-in-out;
    }
}
</style>