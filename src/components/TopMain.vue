<script>
import LifestylesCarousel from './MainBody/TopComps/LifestylesCarousel.vue';
import DisplayCard from './MainBody/TopComps/DisplayCard.vue'
import { gallery } from '../data/index'

export default {
    name: 'TopMain',
    data: () => ({
        ...gallery
    }),
    components: { LifestylesCarousel, DisplayCard },
    computed: {
        galleryFilter() {
            const filteredGallery = gallery.filter(g => (g.labels.includes("Travel") || g.labels.includes("Lifestyle")))
            return filteredGallery
        }
    }
}
</script>


<template>
    <LifestylesCarousel />
    <section id="display-boxes" class="row">
        <div class="col-3">
            <DisplayCard class="small" :object="galleryFilter[0]" />
            <DisplayCard class="small" :object="galleryFilter[1]" />
        </div>
        <div class="col-6">
            <DisplayCard class="big" :object="galleryFilter[2]" />
        </div>
        <div class="col-3">
            <DisplayCard class="small" :object="galleryFilter[3]" />
            <DisplayCard class="small" :object="galleryFilter[4]" />
        </div>
    </section>
</template>

<style lang="scss" scoped>
#display-boxes {
    justify-content: space-between;
    height: 400px;

    &>div {
        flex-wrap: wrap;
        flex-shrink: 0;
        align-content: space-between;
        height: 100%;
    }

    .small {
        height: 50%;
    }

    .big {
        height: 100%;
    }
}
</style>