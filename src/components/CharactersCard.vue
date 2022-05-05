<template>
    <div class="char-card">
        <img :src="thumb" :alt="series">
        <div class="description">
            <span>{{price}}</span>
            <h3>{{series}}</h3>
            <p>{{type}}</p>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        thumb: String,
        price: String,
        series: String,
        type: String
    }
}
</script>

<style lang="scss" scoped>
@import '../style/variables';
@import '../style/general';
.char-card{
    width: calc(100% / 6);
    height: 300px;
    text-align: center;
    padding: 0 20px;
    img{
        width: 100%;
        height: 60%;
        overflow: hidden;
    }
    .description{
        height: 40%;
    }

}

</style>