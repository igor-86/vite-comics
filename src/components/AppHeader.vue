<script>
export default {
    data() {
        return {
            logo: "dc-logo.png",
            menuNavi: [
                {
                    name: "Character",
                    isActive: false,
                },
                {
                    name: "Comics",
                    isActive: true,
                },
                {
                    name: "Movies",
                    isActive: false,
                },
                {
                    name: "Tv",
                    isActive: false,
                },
                {
                    name: "Games",
                    isActive: false,
                },
                {
                    name: "Collectibles",
                    isActive: false,
                },
                {
                    name: "Videos",
                    isActive: false,
                },
                {
                    name: "Fans",
                    isActive: false,
                },
                {
                    name: "News",
                    isActive: false,
                },
                {
                    name: "Shop",
                    isActive: false,
                },

            ],
        }
    },
    components: {

    },
    methods: {

    },
}
</script>

<template>
    <header>
        <div class="container">
            <div class="menu">
                <div class="img-logo">
                    <img src="../assets/img/dc-logo.png" alt="">
                </div>
                <nav class="nav">
                    <ul class="d-flex">
                        <li v-for="(inner, index) in menuNavi">
                            <a href="" :class="{ 'active': inner.isActive }">{{ inner.name }}</a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use "../styles/general.scss" as*;
@use "../styles/partials/variables" as*;

.container {
    .menu {
        width: 100%;
        height: 100px;
        display: flex;
        align-items: center;
        justify-content: space-between;

        .img-logo {
            width: 20%;

            img {
                height: 70px;
                vertical-align: middle;
            }
        }

        .nav {
            display: flex;
            width: 70%;
            justify-content: flex-end;

            li {
                margin: 0 .5rem;

                a {
                    text-transform: uppercase;
                    font-size: .8rem;
                    font-weight: 600;
                    color: #151515;
                    height: 100px;
                    line-height: 100px;

                    &.active {
                        border-bottom: 5px solid $color-primary;
                        color: $color-primary;
                    }
                }
            }
        }
    }
}
</style>