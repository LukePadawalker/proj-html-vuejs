<script>
import { gallery } from '../../../data/_gallery';
import CardPost from './CardPost.vue';
export default {
    name: 'PostsCarousel',
    components: { CardPost },
    data: () => ({ gallery })
}
</script>

<template>
    <div class="header-cards d-flex justify-content-between mb-3">
        <div class="title">
            <h3 class="text-uppercase fw-bold">Featured posts</h3>
        </div>
        <div class="buttons-cards">
            <button class="prev"><i class="fa-solid fa-angle-left fa-lg"></i></button>
            <button class="next"><i class="fa-solid fa-angle-right fa-lg"></i></button>
        </div>
    </div>
    <div class="row-cards">
        <div class="col-card" v-for="(g, id) in gallery" :key="id">
            <CardPost :src="g.src" :title="g.title" :date="g.date" />
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
    display: flex;
    justify-content: space-between;
    width: 100%;
    gap: 10px;
    overflow-x: hidden;


    .col-card {
        flex-basis: calc(100% / 3);
    }
}
</style>