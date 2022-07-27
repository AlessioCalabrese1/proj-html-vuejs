<template>
<main>
    <MainShowcase />
    <Specialties />
    <Staff />
</main>
</template>

<script>
import MainShowcase from './MainShowcase.vue';
import Specialties from './Specialties.vue';
import Staff from './Staff.vue';
export default {
    components: { MainShowcase, Specialties, Staff }
}
</script>

<style lang="scss">
@import "../styles/variables.scss";

main{
    background-color: $backgroundColorMain;
}
</style>