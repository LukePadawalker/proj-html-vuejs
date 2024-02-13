<script>
export default {
    name: 'HeaderLinks'
}
</script>

<template>
    <div class="header-links">
        <div class="container d-flex justify-content-between">
            <div class="news-updates d-flex">
                <h2 class="text-uppercase fs-6 py-1 px-3 mb-0 text-white align-items-center d-flex">news updates</h2>
                <div class="carousel-img p-4"></div>
                <h3 class="text-uppercase fs-6 py-1 px-3 mb-0 align-items-center d-flex fw-bolder">05:35 the best time to
                    have a
                    meal
                </h3>
            </div>
            <div class="links d-flex">
                <ul class="list-unstyled d-flex align-items-center py-1 px-3 mb-0">
                    <li><i class="fa-solid fa-chevron-left mx-4"></i></li>
                    <li><i class="fa-solid fa-chevron-right"></i></li>
                </ul>

                <div class="socials">
                    <ul class="list-unstyled d-flex align-items-center py-2 ps-4 mb-0">
                        <li><a href="#"><i class="fa-brands fa-facebook-f"></i></a></li>
                        <li><a href="#"><i class="fa-brands fa-twitter"></i></a></li>
                        <li><a href="#"><i class="fa-brands fa-instagram"></i></a></li>
                        <li><a href="#"><i class="fa-brands fa-youtube"></i></a></li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.header-links {
    background-color: #BF1D2E;
}

.carousel-img {
    background-color: black;
    height: 40px;
    width: 40px;
}

h2 {
    background-color: #545454;
}

h3 {
    color: #fff;

    &:hover {
        color: #3D3233;
        cursor: pointer;
    }
}

.links {
    ul {
        color: white;

        li {
            &:hover {
                color: #3D3233;
                cursor: pointer;
            }
        }
    }
}

.socials {
    ul {
        list-style: none;
        display: flex;
        flex-direction: row;
        align-items: center;
        gap: 10px;

        li {

            i {
                background-color: #fff;
                width: 30px;
                height: 30px;
                font-size: 16px;
                border-radius: 50%;
                color: #BF1D2E;
                text-align: center;
                line-height: 30px;
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