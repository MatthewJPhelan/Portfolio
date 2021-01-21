<template>
    <div class="header">
        <img src="../assets/imgs/laydown.png" alt="">
    </div>
</template>

<script>
    export default {
        name: "Header"
    }
</script>

<style lang="scss" scoped>
.header {
    display: flex;
    justify-content: center;
    padding-top: 5rem;
    padding-bottom: 1rem;
    background-color: $color-primary;
    overflow: hidden;
}
</style>