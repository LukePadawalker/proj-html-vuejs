<script>

import { gallery } from '../../../data/_gallery';
import CarouselCard from '../TopComps/CarouselCard.vue';

export default {
    name: 'LifestylesCarousel',
    data: () => ({ gallery }),
    components: { CarouselCard },
}

</script>

<template>
    <!-- <div class="buttons-cards">
            <button class="prev"><i class="fa-solid fa-angle-left fa-lg"></i></button>
            <button class="next"><i class="fa-solid fa-angle-right fa-lg"></i></button>
        </div> -->

    <div class="row-cards">
        <div class="col-card" v-for="(g, id) in gallery" :key="id">
            <CarouselCard :src="g.src" :title="g.title" :date="g.date" :labels="g.labels" />
        </div>
    </div>
</template>

<style lang="scss" scoped>
h4 {
    color: #333333;
}

.buttons-cards {
    display: flex;
    gap: 1.2rem;
}

button {
    outline: none;
    border: none;
    height: 2.5rem;
    width: 2.5rem;
    border-radius: 50%;
    background-color: #333333;
    color: white;
    cursor: pointer;

    &:hover {
        background-color: #BF1D2E;
        transition: background-color .3s ease;
    }
}

.row-cards {
    height: 350px;
    display: flex;
    justify-content: space-between;
    width: 100%;
    gap: 10px;
    overflow-x: scroll;


    .col-card {
        width: calc(100% / 4);
    }
}
</style>