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

<style scoped>
.greenish-font-color{
    color: #557174;
    transition: color 0.7s ease-in-out;
}

.light-greenish-font-color {
    color: #9dcbd0;
    transition: color 0.7s ease-in-out;
}

.grey-font-color {
    color: rgba(255, 255, 255, 0.934);
    transition: color 0.7s ease-in-out;
}

.blackish-font-color {
    color: rgba(4, 4, 4, 0.838);
    transition: color 0.7s ease-in-out;
}
</style>
