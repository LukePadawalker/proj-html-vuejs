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
    <div class="background">
        <div class="row-cards">
            <div class="col-card" v-for="(g, id) in gallery" :key="id">
                <CarouselCard :src="g.src" :title="g.title" :date="g.date" :labels="g.labels" />
            </div>
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

.background {
    padding: 2rem 1rem 1rem 1rem;
    background-color: #F3F3F3;
    margin-bottom: 3rem;
}

.row-cards {
    width: 100%;
    min-height: 100px;
    margin-bottom: 20px;
    display: flex;
    flex-wrap: nowrap;
    justify-content: space-around;
    padding-left: 20px;
    padding-right: 20px;

    gap: 20px;
    flex-shrink: 0;
    overflow-x: hidden;
    overflow-y: hidden;


    .col-card {
        width: calc(100% / 4 - 10px);
        flex-shrink: 0;
        height: 380px;
    }
}

.row-cards::-webkit-scrollbar {
    display: none;
}
</style>