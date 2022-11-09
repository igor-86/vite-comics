<script>
export default {
    name: "AppCards",
    props: {
        thumb: String,
        series: String,
        price: String
    },
}
</script>

<template>
    <div class="card">
        <div class="img-card">
            <img :src="thumb" alt="series">

        </div>
        <h3 class="h-1">{{ series }}</h3>
        <h4>{{ price }}</h4>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/general.scss" as*;
@use "../styles/partials/variables" as*;

.card {
    width: calc(100% / 6 - 1rem);
    background-color: lighten($color-current-slide, $amount: 5%);

    .img-card {
        width: 100%;
        height: 180px
    }

    img {
        object-fit: cover;
        object-position: top;
        height: 100%;
        width: 100%;
    }


    h3,
    h4 {
        color: white;
        font-weight: 500;
        font-size: .8rem;
        text-transform: uppercase;

    }

    h3 {
        margin-top: .8rem;
    }
}
</style>