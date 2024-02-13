<script>
import LifestylesCarousel from './MainBody/TopComps/LifestylesCarousel.vue';
import MainNews from './MainBody/TopComps/MainNews.vue';
import LifestyleStories from './MainBody/TopComps/LifestyleStories.vue';

import { gallery } from '../data/index'

export default {
    name: 'TopMain',
    components: { LifestylesCarousel, MainNews, LifestyleStories }
}
</script>


<template>
    <LifestylesCarousel />
    <MainNews />
    <LifestyleStories />
</template>

<style lang="scss" scoped></style>
