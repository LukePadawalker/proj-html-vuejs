<script>
import LifestylesCarousel from './MainBody/TopComps/MainLifestyles.vue';

export default {
    name: 'TopMain',
    components: { LifestylesCarousel }
}
</script>

<template>
    <LifestylesCarousel />
    <section id="display-boxes">

    </section>
</template>

<style lang="scss" scoped>
#display-boxes {
    height: 300px;
    background-color: bisque;
}
</style>
