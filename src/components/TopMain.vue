<script>
import LifestylesCarousel from './MainBody/TopComps/MainLifestyles.vue';
import { gallery } from '../data/index'

export default {
    name: 'TopMain',
    data: () => ({
        ...gallery
    }),
    components: { LifestylesCarousel },
    computed: {
        galleryFilter() {
            return filteredGallery = gallery.filter(g => (g.labels.includes("Travel" || "Lifestyle")))
        }
    }
}
</script>


<template>
    <LifestylesCarousel />
    <section id="display-boxes" class="row">
        <div class="col-3 d-flex ">
            <div class="box-s"><img src="" alt=""></div>
            <div class="box-s"></div>
        </div>
        <div class="col-6 box-xl">

        </div>
        <div class="col-3 d-flex">
            <div class="box-s"></div>
            <div class="box-s"></div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
#display-boxes {
    height: 300px;
    background-color: bisque;
    justify-content: space-between;

    &>div {
        flex-wrap: wrap;
        align-content: space-between;
    }
}

.box-s {
    width: 100%;
    height: 50%;
    border: 1px solid black;
}

.box-xl {
    width: 50%;
    height: 100%;
    border: 1px solid black;
}
</style>