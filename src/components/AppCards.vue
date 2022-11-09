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
        <h3>{{ series }}</h3>
        <h4>{{ price }}</h4>
    </div>
</template>

<style lang="scss" scoped>
.card {
    width: calc(100% / 6 - 1rem);

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
        margin-top: .5rem;
    }
}
</style>