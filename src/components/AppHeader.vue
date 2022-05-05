<template>
  <header>
    <div class="logo">
      <img src="../assets/images/dc-logo.png" alt="Logo DC">
    </div>
    <nav>
      <ul>
        <li v-for="item in links" :key="item">
          <a href="#">
            <div class="choice-button">{{item}}</div>
          </a>
        </li>
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
        "Characters",
        "Comics",
        "Movies",
        "Tv",
        "Games",
        "Collectibles",
        "Videos",
        "Fans",
        "News",
        "Shop"
      ]
    }
  }
}

</script>

<style lang="scss" scoped>
  @import '../style/variables';
  @import '../style/general';
  header{
    height: 120px;
    @include my-flex;
  }
  ul{
    @include my-flex;
    line-height: 120px;
  }
  li{
      list-style-type: none;
      padding: 0 10px;
    a{
      text-decoration: none;
      text-transform: uppercase;
      color: $colortextheader;
      font-weight: bold;
      .choice-button{
        position: relative;
        display: flex;
        justify-content: center;
        &:hover{
          color: $colortextactive;
          &::after{
            position: absolute;
            bottom: 0;
            content: '';
            width: 100%;
            height: 3px;
            background-color: $colortextactive;
          }
        }
      }
    }
  }
</style>
