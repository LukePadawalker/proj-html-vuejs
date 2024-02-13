<script>
import LifestylesCarousel from './MainBody/TopComps/LifestylesCarousel.vue';
import MainNews from './MainBody/TopComps/MainNews.vue';

import { gallery } from '../data/index'

export default {
    name: 'TopMain',
    components: { LifestylesCarousel, MainNews }
}
</script>


<template>
    <LifestylesCarousel />
    <MainNews />
</template>

<style lang="scss" scoped></style>
