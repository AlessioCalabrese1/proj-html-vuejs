<template>
<main>
    <MainShowcase />
    <Specialties />
</main>
</template>

<script>
import MainShowcase from './MainShowcase.vue';
import Specialties from './Specialties.vue';
export default {
    components: { MainShowcase, Specialties }
}
</script>

<style lang="scss">
@import "../styles/variables.scss";

main{
    background-color: $backgroundColorMain;
}
</style>