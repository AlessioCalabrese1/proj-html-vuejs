<template>
<main>
    <MainShowcase />
    <Specialties />
    <Staff />
    <Events />
    <Stats />
    <News />
    <Testimonials />
    <Video />
    <ComunicateWithUs />
</main>
</template>

<script>
import MainShowcase from './MainShowcase.vue';
import Specialties from './Specialties.vue';
import Staff from './Staff.vue';
import Events from './Events.vue';
import Stats from './Stats.vue';
import News from './News.vue';
import Testimonials from './Testimonials.vue';
import Video from './Video.vue';
import ComunicateWithUs from './ComunicateWithUs.vue';
export default {
    components: { MainShowcase, Specialties, Staff, Events, Stats, News, Testimonials, Video, ComunicateWithUs }
}
</script>

<style lang="scss">
@import "../styles/variables.scss";

main{
    background-color: $backgroundColorMain;
}
</style>