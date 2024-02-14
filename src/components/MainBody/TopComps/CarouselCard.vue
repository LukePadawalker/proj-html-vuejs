<script>

export default {
    name: 'CarouselCard',
    props: {
        src: String,
        title: String,
        date: String,
        labels: Array
    }
}

</script>

<template>
    <div class="card border-0">
        <img :src="`src/assets/img/${src}`" :alt="title" class="card-img-top">
        <div id="labels" class="p-4">
            <a href="#" class="label" v-for="label in labels">{{ label }}</a>
        </div>
        <div class="card-body text-center rounded-bottom">
            <h5 class="card-title fw-bold">{{ title }}</h5>
            <span class="date text-secondary fw-bold">{{ date }}</span>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.card-body {
    background-color: #F3F3F3;
}

h5:hover {
    color: #BF1D2E;
}
</style>