<script>
import HeaderLinks from './Header/HeaderLinks.vue'
export default {
    name: 'AppHeader',
    components: { HeaderLinks }
}
</script>

<template>
    <header>
        <HeaderLinks />
    </header>
</template>

<style lang="scss" scoped>
header {
    background-color: blue;
    width: 100%;
}
</style>
