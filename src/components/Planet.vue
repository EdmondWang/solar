<template>
    <div v-bind:style="{ width: radius + 'px'}">
        {{name}}
    </div>
</template>
<script>
export default {
    name: 'Planet',
    props: {
        name: String,
        radius: Number
    }
}
</script>
<style lang="sass" scoped>
$box-model: border-box;
div {
    box-sizing: $box-model;
    border-radius: 50%;
}
</style>