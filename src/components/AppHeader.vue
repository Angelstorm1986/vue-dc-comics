<template>
  <header>
    <div class="logo">
      <img src="../assets/images/dc-logo.png" alt="Logo DC">
    </div>
    <nav>
      <ul>
        <li v-for="(item, index) in links" :key="index">
          <a href="#">
            <div class="choice-button">{{item.testo}}</div></a></li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'AppHeader',
  data() {
    return {
      links: [
        {
          testo: "Characters",
          active: false
        },
        {
          testo: "Comics",
          active: true
        },
        {
          testo: "Movies",
          active: false
        },
        {
          testo: "Tv",
          active: false
        },
        {
          testo: "Games",
          active: false
        },
        {
          testo: "Collectibles",
          active: false
        },
        {
          testo: "Videos",
          active: false
        },
        {
          testo: "Fans",
          active: false
        },
        {
          testo: "News",
          active: false
        },
        {
          testo: "Shop",
          active: false
        }
      ]
    }
  }
}

</script>

<style lang="scss">
  @import '../style/variables';
  @import '../style/general';
  header{
    height: 120px;
    @include my-flex;
    justify-content: space-around;
  }
  ul{
    @include my-flex;
    justify-content: center;
    line-height: 120px;
  }
  li{
      list-style-type: none;
      padding: 0 10px;
    a{
      text-decoration: none;
      color: $colortextheader;
      font-weight: bold;
      .choice-button{
        position: relative;
        display: flex;
        justify-content: center;
        &:hover::after{
          position: absolute;
          bottom: 0;
          content: '';
          width: 100%;
          height: 3px;
          background-color: $coloractive;
        }
      }
    }
  }
</style>
