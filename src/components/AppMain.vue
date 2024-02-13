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
        <BottomMain />
    </div>
</template>

<style lang="scss"></style>
