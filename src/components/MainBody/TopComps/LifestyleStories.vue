<script>
export default {
    name: 'Lifestyle & Stories'
}
</script>

<template>
    <section class="my-5">
        <div class="section-header d-flex justify-content-between">
            <h3 class="section-title">Lifestyle & Stories</h3>
            <div class="btn-group">
                <button>All</button>
                <button>Lifestyle</button>
                <button>Stories</button>
            </div>
        </div>

        <div class="section-image d-flex">
            <div class="left-poster">
                <img class="poster" src="../../../assets/img/best-places.webp" alt="Lifestyle">
                <div class="label">Lifestyle</div>
                <div class="info">
                    <p>
                        <span><i class="fa-solid fa-user"></i> Demo </span>
                        <span><i class="fa-solid fa-calendar-days"></i> December 25, 2022</span>
                    </p>
                    <h5>Place For A Road Trip</h5>
                </div>
            </div>
            <div class="right-gallery">
                <div class="card-gallery d-flex align-items-center gap-3">
                    <img src="../../../assets/img/music-love.webp" alt="Culture">
                    <div class="gallery-info">
                        <p>
                            <span><i class="fa-solid fa-user"></i> Demo </span>
                            <span><i class="fa-solid fa-calendar-days"></i> December 25, 2022</span>
                        </p>
                        <h5>Place For A Road Trip</h5>
                    </div>
                </div>
                <div class="card-gallery"></div>
                <div class="card-gallery"></div>
            </div>
        </div>

    </section>
</template>

<style lang="scss" scoped>
@use '../../../assets/scss/vars' as *;

.section-title {
    text-transform: uppercase;
    color: $dark-gray;
}

button {
    text-transform: uppercase;
    color: $white;
    background-color: #545454;
    margin-left: 20px;
    border-radius: 5px;
    border: 1px solid currentColor;
    padding: 5px 20px;
}

.section-image {
    margin-top: 20px;
    width: 100%;
    height: 500px;

}

.left-poster {
    width: 60%;
    height: 100%;

    position: relative;
}

.left-poster::before {
    position: absolute;
    top: 0;
    right: 0;
    left: 0;
    bottom: 0;
    background-color: rgba(0, 0, 0, 0.5);
    border-radius: 5px;
    content: '';
}

.poster {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 5px;
}

.label {
    background-color: $white;
    color: $dark-gray;
    font-size: 14px;
    font-weight: 500;
    padding: 3px 15px;
    border-radius: 7px;
    cursor: pointer;

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

.right-gallery {
    padding: 0 20px;
}

.right-gallery img {
    width: 200px;
    border-radius: 5px;
}

.gallery-info {
    color: $dark-gray;
    font-weight: 600;
}
</style>