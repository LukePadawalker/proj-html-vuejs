<script>
export default {
    name: "NavMenu",
    data: () => ({
        openCanvas: false,
    }),
    computed: {
        toggleCanvas() {
            this.openCanvas = !this.openCanvas
        }
    }
}
</script>

<template>
    <a href="#" type="button" @click="toggleCanvas">
        <i class="fa-solid fa-bars fs-2"></i>
    </a>

    <div class="offcanvas offcanvas-start" :class="{ 'show': openCanvas }" id="offcanvasMenu">
        <div class="offcanvas-header">
            <div>
                <i class="fa-solid fa-xmark" type="button" @click="toggleCanvas"></i>
            </div>
        </div>
        <div class="offcanvas-body">
            <img class="offcanvas-logo" src="../../assets/img/anime-logo.webp" alt="">
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quo dolores maiores ullam aliquam consectetur rerum.
            </p>
            <picture class="offcanvas-pics d-flex">
                <img src="../../assets/img/music-love.webp" alt="">
                <img src="../../assets/img/best-places.webp" alt="">
                <img src="../../assets/img/anime-fashion.webp" alt="">
            </picture>
            <div class="socials">
                <ul class="list-unstyled d-flex align-items-center py-2 ps-4 mb-0">
                    <li><a href="#"><i class="fa-brands fa-facebook-f"></i></a></li>
                    <li><a href="#"><i class="fa-brands fa-twitter"></i></a></li>
                    <li><a href="#"><i class="fa-brands fa-instagram"></i></a></li>
                    <li><a href="#"><i class="fa-brands fa-youtube"></i></a></li>
                </ul>
            </div>
        </div>
        <div :class="{ 'canvas-overlay': openCanvas }"></div>
    </div>
</template>

<style lang="scss" scoped>
.canvas-overlay {
    position: fixed;
    top: 0;
    bottom: 0;
    left: 45vw;
    right: 0;
    z-index: 1;
    background-color: rgba(0, 0, 0, 0.7);
}

a {
    color: #545454;

    &:hover {
        color: #BF1D2E;
    }
}

#offcanvasMenu {
    width: 45vw;

    .offcanvas-header {
        position: relative;

        div {
            position: absolute;
            top: 0px;
            left: 100%;

            width: 50px;
            height: 50px;
            background-color: rgb(94, 93, 93);

            i.fa-xmark {
                position: absolute;
                top: 50%;
                left: 50%;
                translate: -50% -50%;
                z-index: 2;

                color: white;

                padding: 10px;
                border: 2px solid white;
            }
        }
    }

    .offcanvas-body {
        padding: 50px 30px;
        text-align: center;


        .offcanvas-logo {
            width: 300px;
            height: auto;
            margin: 50px 0;
        }


        picture {
            margin: 50px 0;
            width: 100%;
            height: 125px;
            justify-content: center;

            img {
                border-radius: 10px;
                padding: 5px;
                object-fit: cover;

            }
        }
    }
}

.socials {
    display: flex;
    align-items: center;
    justify-content: center;

    ul {
        list-style: none;
        display: flex;
        flex-direction: row;
        align-items: center;
        gap: 10px;

        li {

            i {
                background-color: #bf1d2e;
                width: 40px;
                height: 40px;
                font-size: 16px;
                border-radius: 50%;
                color: #ffffff;
                text-align: center;
                line-height: 40px;
                transition: color 0.3s, background-color 0.4s;

                &:hover {
                    color: #fff;
                    background-color: #545454;
                }
            }
        }
    }
}
</style>