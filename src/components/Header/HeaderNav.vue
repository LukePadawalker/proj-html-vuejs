<script>
import SearchOffcanvas from './SearchOffcanvas.vue';

export default {
    name: 'HeaderNav',
    data: () => ({
        links: [
            {
                name: 'home',
                icon: 'fa-solid fa-house-chimney',
                dropDown: null
            },
            {
                name: 'about us',
                icon: 'fa-solid fa-user',
                dropDown: null
            },
            {
                name: 'lifestyle',
                icon: 'fa-solid fa-suitcase',
                dropDown: 'fa-solid fa-angle-down'
            },
            {
                name: 'stories',
                icon: 'fa-solid fa-book-open-reader',
                dropDown: 'fa-solid fa-angle-down'
            },
            {
                name: 'pages',
                icon: 'fa-solid fa-book',
                dropDown: null
            },
            {
                name: 'contact us',
                icon: 'fa-solid fa-envelope',
                dropDown: null
            }
        ]
    }),
    components: {
        SearchOffcanvas
    }

}
</script>

<template>
    <div class="header-nav">
        <div class="container py-3">
            <div class="row align-items-center">
                <div class="col-2"><a href="#"><i class="fa-solid fa-bars fs-2"></i></a></div>
                <div class="col-8">
                    <ul class="list-unstyled d-flex flex-row justify-content-center mb-0">
                        <li v-for="(link, i) in links" :key="link.name" class="text-uppercase mx-2 fs-6">
                            <a href="#" class="text-decoration-none fw-semibold"><i :class="link.icon" class="px-2"></i>{{
                                link.name
                            }}<i class="ms-2" :class="link.dropDown"></i></a>
                        </li>
                    </ul>
                </div>
                <div class="col-2 d-flex justify-content-end">
                    <SearchOffcanvas />
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.header-nav {
    border-top: 2px solid #F3F3F3;
    background-color: #fff;
}

a {
    color: #545454;

    &:hover {
        color: #BF1D2E;
    }
}

.col-8 {
    a {
        color: #000;

        &:hover {
            color: #BF1D2E;
        }
    }
}
</style>