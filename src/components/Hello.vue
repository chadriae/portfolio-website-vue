<template>
    <div class="text-left">
        <header class="uppercase font-bold text-3xl mb-2" :class="(mode === 'dark') ? 'grey-font-color' : 'greenish-font-color'">Christophe Adriaensens</header>
        <p class="font-bold text-xl mb-2" :class="(mode === 'dark') ? 'light-greenish-font-color' : 'blackish-font-color'">I'm a junior full-stack developer.</p>
        <p class="text-gray-700 ml-2" :class="(mode === 'dark') ? 'light-greenish-font-color' : 'blackish-font-color'">Based in Ghent.</p>
    </div>
</template>

<script>
export default {
    props: ['mode']
}
</script>

<style scoped lang="scss">
@import "../styles/_variables.scss";

.greenish-font-color{
    color: $greenish-font-color;
    transition: $font-color-transition;
}

.light-greenish-font-color {
    color: $light-greenish-font-color;
    transition: $font-color-transition;
}

.grey-font-color {
    color: $white-color;
    transition: $font-color-transition;
}

.blackish-font-color {
    color: $dark-font-color;
    transition: $font-color-transition;
}
</style>
