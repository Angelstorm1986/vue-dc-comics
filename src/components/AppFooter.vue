<template>
    <footer>
        <div class="products">
            <div class="list" v-for="(prodotto, index) in products" :key="index">
                <img :src="prodotto.image" width="30" height="30" :alt="prodotto.nome">
                <span>{{prodotto.nome}}</span>
            </div>
        </div>
        <div class="alldc">
            <div class="utilities">
                <div>
                    <h2>dc comics</h2>
                    <ul>
                        <li v-for="list in world" :key="list">{{list}}</li>
                    </ul>
                </div>
                <div>
                    <h2>dc</h2>
                    <ul>
                        <li v-for="item in all" :key="item">{{item}}</li>
                    </ul>
                </div>
                <div>
                    <h2>sites</h2>
                    <ul>
                        <li v-for="site in sites" :key="site">{{site}}</li>
                    </ul>
                </div>
                <div>
                    <h2>shop</h2>
                    <ul>
                        <li v-for="choice in shop" :key="choice">{{choice}}</li>
                    </ul>
                </div>
            </div>
            <img src="../assets/images/dc-logo-bg.png" width="500" height="500" alt="DC Logo">
        </div>
        <div>

        </div>
    </footer>
</template>

<script>
export default {
    name: 'AppFooter',
    data() {
        return {
            products: [
                {
                    image: "./images/buy-comics-digital-comics.png",
                    nome: "Digital Comics"
                },
                {
                    image: "./images/buy-comics-merchandise.png",
                    nome: "DC Merchandise"
                },
                {
                    image: "./images/buy-comics-subscriptions.png",
                    nome: "Subscription"
                },
                {
                    image: "./images/buy-comics-shop-locator.png",
                    nome: "Comic shop locator"
                },
                {
                    image: "./images/buy-dc-power-visa.svg",
                    nome: "DC Power visa"
                }
            ],
            world: [
                "Characters", 
                "Comics",
                "Movies",
                "Tv",
                "Games",
                "Collectibles",
                "Videos",
                "Fans",
                "News"
            ],
            all: [
                "Terms Of Use", 
                "Privacy policy (New)",
                "Ad Choices",
                "Advertising",
                "Jobs",
                "Subscriptions",
                "Talent Workshops",
                "CPSC Certificates",
                "Ratings",
                "Shop Help",
                "Contact Us"
            ],
            sites: [
                "DC", 
                "MAD Magazine",
                "DC Kids",
                "DC Universe",
                "DC Power Visa"
            ],
            shop: [
                "Shop DC",
                "Shop DC Collectibles" 
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../style/variables';
@import '../style/general';
.products{
    height: 120px;
    @include my-flex;
    background-color: $bgproducts;
    color: $colortextmain;

}
.list{
    @include my-flex;
    span{
        padding-left: 10px;
    }
}
.alldc{
    @include my-flex;
    height: 350px;
    overflow: hidden;
    background-image: url(../assets/images/footer-bg.jpg);
}
.utilities{
    width: 30%;
    color: $colortextmain;
    display: flex;
    flex-wrap: wrap;
    div{
        padding: 0 5px;
    }
}
h2{
    text-transform: uppercase;
    font-size: 20px;
}
li{
    list-style-type: none;
    font-size: 15px;
}
</style>