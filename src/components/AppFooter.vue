<template>
    <footer>
        <div class="products">
            <div class="list" v-for="(prodotto, index) in products" :key="index">
                <img src="{'../assets/images/' + prodotto.image}" :alt="prodotto.nome">
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
            image: "buy-comics-digital-comics.png",
            nome: "Digital Comics"
        },
        {
            image: "buy-comics-merchandise.png",
            nome: "DC Merchandise"
        },
        {
            image: "buy-comics-subscription.png",
            nome: "Subscription"
        },
        {
            image: "buy-comics-shop-locator.png",
            nome: "Comic shop locator"
        },
        {
            image: "buy-dc-power-visa.png",
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