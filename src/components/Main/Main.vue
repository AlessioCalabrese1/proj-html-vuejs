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
    <SponsorLogos />
</main>
</template>

<script>
import MainShowcase from './MainShowcase/MainShowcase.vue';
import Specialties from './Specialties/Specialties.vue';
import Staff from './Staff/Staff.vue';
import Events from './Events/Events.vue';
import Stats from './Stats/Stats.vue';
import News from './News/News.vue';
import Testimonials from './Testimonials/Testimonials.vue';
import Video from './Video/Video.vue';
import ComunicateWithUs from './ComunicateWithUs/ComunicateWithUs.vue';
import SponsorLogos from './SponsorLogos/SponsorLogos.vue';
export default {
    components: { MainShowcase, Specialties, Staff, Events, Stats, News, Testimonials, Video, ComunicateWithUs, SponsorLogos }
}
</script>

<style lang="scss">
@import "../../styles/variables.scss";

main{
    background-color: $backgroundColorMain;
}
</style>