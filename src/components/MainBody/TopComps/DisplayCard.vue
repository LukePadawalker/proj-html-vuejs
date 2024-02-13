<script>

export default {
    name: "DisplayCard",
    props: {
        object: Object
    }
}

</script>

<template>
    <div class="card">
        <img :src="`src/assets/img/${object.src}`" :alt="title">
        <div id="labels">
            <span class="label" v-for="label in object.labels">{{ label }}</span>
        </div>
        <div>
            <span>
                <i class="fa-solid fa-user"></i> demo
            </span>
            <span>{{ object.date }}</span>
            <span>{{ object.title }}</span>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.card {
    background-color: transparent;
    flex-shrink: 0;
    flex-grow: 1;
    padding: 5px;

    width: 100%;
}

.label {
    padding: 5px 20px;
    background-color: white;
    border-radius: 5px;
    margin: 5px;
}

img {
    width: 100%;
    height: 100%;

    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    z-index: -1;
}
</style>