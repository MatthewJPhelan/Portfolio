<template>
    <div class="terminal">
        <div class="terminal-input">
            mattyjphelan ~ % {{ input }}
        </div>
        <div class="terminal-output">
            <slot />
        </div>
    </div>
</template>

<script>
    export default {
        name: "Terminal",
        props: {
            input:{
                type: String
            }
        }
    }
</script>

<style lang="scss" scoped>
.terminal {
    margin: 1rem 0;
}
</style>