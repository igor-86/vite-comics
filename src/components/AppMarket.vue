<script>
export default {
    name: "AppMarket",
    data() {
        return {
            listMarket: [
                {
                    imgMarket: "buy-comics-digital-comics.png",
                    title: "Digital comics"
                },
                {
                    imgMarket: "buy-comics-merchandise.png",
                    title: "Dc Merchandise"
                },
                {
                    imgMarket: "buy-comics-subscriptions.png",
                    title: "Subscription"
                },
                {
                    imgMarket: "buy-comics-shop-locator.png",
                    title: "Comics shop locator"
                },
                {
                    imgMarket: "buy-dc-power-visa.svg",
                    title: "Digital comics"
                }
            ]
        }
    },
    methods: {
        getImage(url) {
            return new URL(url, import.meta.url).href;
        }
    },
}
</script>

<template>
    <div class="container pad-l">
        <div class="row">
            <div class="market-card" v-for="(inner, index) in listMarket" :key="index">
                <img :src="getImage(`../assets/img/${inner.imgMarket}`)" alt="">
                <h3>{{ inner.title }}</h3>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as*;

.pad-l {
    padding: 3rem 1rem;


    .market-card {
        width: calc(100% / 5 - 1rem);
        display: flex;
        align-items: center;

        img {
            width: 80px;
            height: 80px;
        }

        h3 {
            margin-left: .8em;
            color: white;
            font-weight: 600;
            text-transform: uppercase;
        }
    }
}
</style>