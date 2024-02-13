<script>
import DisplayCard from './MainBody/TopComps/DisplayCard.vue'

export default {
    name: 'MainNews',
    data: () => ({
        ...gallery
    }),
    components: { DisplayCard },
    computed: {
        galleryFilter() {
            const filteredGallery = gallery.filter(g => (g.labels.includes("Travel") || g.labels.includes("Lifestyle")))
            return filteredGallery
        }
    }
}
</script>

<template>
    <div class="container">
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
    </div>
</template>

<style lang="scss">
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
