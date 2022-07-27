<template>
<main>
    <MainShowcase />
    <Specialties />
    <Staff />
    <Events />
    <Stats />
    <News />
</main>
</template>

<script>
import MainShowcase from './MainShowcase.vue';
import Specialties from './Specialties.vue';
import Staff from './Staff.vue';
import Events from './Events.vue';
import Stats from './Stats.vue';
import News from './News.vue';
export default {
    components: { MainShowcase, Specialties, Staff, Events, Stats, News }
}
</script>

<style lang="scss">
@import "../styles/variables.scss";

main{
    background-color: $backgroundColorMain;
}
</style>