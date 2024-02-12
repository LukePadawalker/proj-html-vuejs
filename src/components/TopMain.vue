<script>
import MainLifestylesVue from './MainBody/TopComps/MainLifestyles.vue';
import MainNewsVue from './MainBody/TopComps/MainNews.vue';
export default {
    name: 'TopMain',
    components: { MainLifestylesVue, MainNewsVue }
}
</script>

<template>
    <MainLifestylesVue />
    <MainNewsVue />
</template>

<style lang="scss"></style>
