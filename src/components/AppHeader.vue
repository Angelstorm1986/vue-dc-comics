<template>
  <header>
    <div class="logo">
      <img src="../assets/images/dc-logo.png" alt="Logo DC">
    </div>
    <nav>
      <ul>
        <li v-for="choice in choices" :key="choice">
          <a href="#">
            <div class="choice-button" :class="{ active : choice.active }">{{choice.text}}</div>
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
      choices: [
        {
          text: "Characters",
          active: false
        },
        {
          text: "Comics",
          active: true
        },
        {
          text: "Movies",
          active: false
        },
        {
          text: "Tv",
          active: false
        },
        {
          text: "Games",
          active: false
        },
        {
          text: "Collectibles",
          active: false
        },
        {
          text: "Videos",
          active: false
        },
        {
          text: "Fans",
          active: false
        },
        {
          text: "News",
          active: false
        },
        {
          text: "Shop",
          active: false
        }
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
        // &:hover{
        //   color: $colortextactive;
        //   &::after{
        //     position: absolute;
        //     bottom: 0;
        //     content: '';
        //     width: 100%;
        //     height: 3px;
        //     background-color: $colortextactive;
        //   }
        // }
      }
    }
  }
  .active{
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
</style>
