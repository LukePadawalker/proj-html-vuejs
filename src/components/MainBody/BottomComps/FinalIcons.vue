<script>
export default {
    name: 'FinalIcons'
}
</script>

<template>
    <div class="container-fluid">
        <div class="gallery-row">
            <div class="gallery-col" id="fashion">
                <figure>
                    <img src="../../../assets/img/anime-fashion.webp" alt="">
                </figure>
                <div class="gallery-title text-center">
                    <h4>Fashion</h4>
                    <p class="post">3 post</p>
                </div>
            </div>

            <div class="gallery-col" id="culture">
                <figure>
                    <img src="../../../assets/img/success-story.webp" alt="">
                </figure>
                <div class="gallery-title text-center ">
                    <h4>Culture</h4>
                    <p class="post">3 post</p>
                </div>
            </div>

            <div class="gallery-col" id="food">
                <figure>
                    <img src="../../../assets/img/healthy-foods.webp" alt="">
                </figure>
                <div class="gallery-title text-center">
                    <h4>Food</h4>
                    <p class="post">3 post</p>
                </div>
            </div>

            <div class="gallery-col" id="lifestyle">
                <figure>
                    <img src="../../../assets/img/visit-france.webp" alt="">
                </figure>
                <div class="gallery-title text-center">
                    <h4>Lifestyle</h4>
                    <p class="post">3 post</p>
                </div>
            </div>

            <div class="gallery-col" id="stories">
                <figure>
                    <img src="../../../assets/img/travel-alone.webp" alt="">
                </figure>
                <div class="gallery-title text-center">
                    <h4>Stories</h4>
                    <p class="post">3 post</p>
                </div>
            </div>

            <div class="gallery-col" id="travel">
                <figure>
                    <img src="../../../assets/img/best-places.webp" alt="">
                </figure>
                <div class="gallery-title text-center">
                    <h4>Travel</h4>
                    <p class="post">3 post</p>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss">
.gallery-row {
    display: flex;
    margin: 0 -1rem;
}

.gallery-title {
    color: white;
    text-transform: uppercase;
    font-weight: 700;
    padding: 50px 70px;

    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}

.gallery-col {
    border-radius: 5px;
    margin: 1rem;
    width: calc(100% / 6 - 2rem);
    height: 250px;
    cursor: pointer;
    background-position: center;
    background-size: cover;

    /*Position relative per opacità statica */
    position: relative;
}

.gallery-col img {
    border-radius: 5px;
    width: 100%;
    height: 250px;
    object-fit: cover;
    overflow: hidden;
}

/* Opacity nera statica */
.gallery-col::before {
    position: absolute;
    top: 0;
    right: 0;
    left: 0;
    bottom: 0;
    background-color: rgba(0, 0, 0, 0.5);
    border-radius: 5px;
    content: '';
}

/* Opacity rossa all'hover */
.gallery-col figure {
    background-color: #bf1d2e;
    border-radius: 5px;
}

.gallery-col figure img {
    opacity: 1;
    -webkit-transition: .3s ease-in-out;
    transition: background-color .3s ease-in-out;
}

.gallery-col:hover img {
    opacity: .3;
}

.gallery-col:hover .gallery-title {
    border: 1px solid white;
}

.post {
    visibility: hidden;
}

.gallery-col:hover .post {
    visibility: visible;
}
</style>
