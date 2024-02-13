<script>
import BottomMain from './BottomMain.vue';
import TopMain from './TopMain.vue';
export default {
    name: 'AppMain',
    components: { BottomMain, TopMain }
}
</script>

<template>
    <div class="container">
        <TopMain />
    </div>
    <div class="banner">
        <div class="container">
            <img src="../assets/img/page-banner-1-768x71.webp" alt="banner" class="rounded">
        </div>
    </div>
    <div class="container">
        <BottomMain />
    </div>
</template>

<style lang="scss" scoped>
.banner {
    padding: 2rem;
    background-color: #F3F3F3;
    margin: 3rem 0;
    text-align: center;

    img {
        width: 100%;
    }
}
</style>
