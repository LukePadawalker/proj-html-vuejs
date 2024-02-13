<script>
export default {
    name: "SearchOffcanvas"

}
</script>

<template>
    <a href="#" type="button" data-bs-toggle="offcanvas" data-bs-target="#offcanvasTop" aria-controls="offcanvasTop">
        <i class="fa-solid fa-magnifying-glass fs-2"></i>
    </a>

    <div class="offcanvas" tabindex="-1" id="offcanvasTop">
        <div class="offcanvas-body d-flex">
            <form>
                <input type="text" placeholder="Search...">
            </form>
            <span type="button" class="btn-close" data-bs-dismiss="offcanvas" aria-label="Close"></span>
        </div>
    </div>
</template>

<style lang="scss" scoped>
a {
    color: #545454;

    &:hover {
        color: #BF1D2E;
    }
}

#offcanvasTop {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: transparent;

    height: 100vh;
    width: 100vw;


    .offcanvas-body {
        position: absolute;
        top: 50%;
        left: 20%;
        z-index: 1;

        background-color: rgba(255, 255, 255, 0.3);

        align-items: center;
        justify-content: center;

        input {
            text-align: center;
            background-color: transparent;
            width: 50vw;

            border: 0;
            border-bottom: 2px solid white;
            margin-right: 50px;

            font-size: 2rem;
            font-weight: 700;
            color: white;
        }

        span.btn-close {
            opacity: 1;
            color: white;
            font-size: 1.5rem;
        }

    }
}
</style>