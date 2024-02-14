<script>

import { gallery } from '../../data/_gallery'

export default {
    name: 'CarouselHeaderTop',
    data: () => ({
        gallery,
        activeCard: 1,
    })
    //     computed: {
    //         setActiveCard(id) {
    //             const nextId = id++
    //             this.activeCard === nextId ? true : false
    //         }
    //     },
    //     methods: {
    //     },
    //     mounted: {
    //         startAutoplay() {
    //             setInterval(setActiveCard(this.id), 3000);
    //         }
    //     }
}
</script>
<!-- :class="{ 'd-block': setActiveCard(id) }" -->
<template>
    <div v-for="{ id, title, src } in this.gallery" :key="id" class="d-none" :class="{ 'd-block': activeCard === id }">
        <picture class="carousel-img p-4">
            <img :src="`../../assets/img/${src}`" :alt="title">
        </picture>
        <h3 class="text-uppercase fs-6 py-1 px-3 mb-0 align-items-center d-flex fw-bolder"> 05:35 {{ title }}
        </h3>
    </div>
</template>

<style lang="scss" scoped>
.carousel-img {
    background-color: black;
    height: 40px;
    width: 40px;
}



h3 {
    color: #fff;

    &:hover {
        color: #3D3233;
        cursor: pointer;
    }
}
</style>