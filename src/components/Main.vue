<template>
<main>
    <MainShowcase />
    <Specialties />
    <Staff />
    <Events />
</main>
</template>

<script>
import MainShowcase from './MainShowcase.vue';
import Specialties from './Specialties.vue';
import Staff from './Staff.vue';
import Events from './Events.vue';
export default {
    components: { MainShowcase, Specialties, Staff, Events }
}
</script>

<style lang="scss">
@import "../styles/variables.scss";

main{
    background-color: $backgroundColorMain;
}
</style>