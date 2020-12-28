<script>
    export default {
        name: "SplitSection",
        props: {
            title: {
                type: String,
                required: true,
            },
            tagLine: {
                type: String,
                required: true,
            },
            description: {
                type: String,
                required: true,
            },
            imageLocation: {
                type: String,
                required: true,
            },
        }
    }
</script>

<template>
    <section class="split-section">
        <div class="split-section-card" :style="{ backgroundImage: `url('${imageLocation}')` }">
            <!-- <slot name="split-section-image"></slot> -->
        </div>
        <div class="split-section-content">
            <div class="split-section-content__title">{{ title }}</div>
            <div class="split-section-content__tagline">{{ tagline }}</div>
            <div class="split-section-content__description">{{ description }}</div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
.split-section {
    margin-bottom: 4rem;
    display: flex;
    justify-content: space-between;

    &-card{
        border-radius: 1rem;
        box-shadow: 4px 4px 16px -8px rgba(0,0,0,0.75);
        min-width: 200px;
        max-width: 450px;
        height: 400px;

        &__img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }
}
</style>