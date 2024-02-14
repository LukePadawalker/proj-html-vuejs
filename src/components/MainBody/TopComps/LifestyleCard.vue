<script>
export default {

}
</script>

<template>
    <img class="poster" src="../../../assets/img/best-places.webp" alt="Lifestyle">
    <div class="label">Lifestyle</div>
    <div class="info">
        <div>
            <span><i class="fa-solid fa-user"></i> demo </span>
            <span><i class="fa-solid fa-calendar-days"></i> December 25, 2022</span>
        </div>
        <h5>Place For A Road Trip</h5>
    </div>
</template>

<style lang="scss" scoped>
@use '../../../assets/scss/vars' as *;

.poster {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 5px;
}

.label {
    color: $dark-gray;
    font-size: 14px;
    font-weight: 500;

    position: absolute;
    top: 15px;
    left: 15px;
}

.info {
    color: $white;
    font-weight: 600;

    position: absolute;
    bottom: 50px;
    left: 20px;
}
</style>