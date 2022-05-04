<template>
  <header>
    <div class="logo">
      <img src="../assets/images/la-molisana-logo.png" alt="Logo La Molisana">
    </div>
    <nav>
      <ul>
        <li v-for="(item, index) in links" :key="index" class="{'selected' : item.active}">{{item.testo}}</li>
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
          testo: "Home",
          active: false
        },
        {
          testo: "Prodotti",
          active: true
        },
        {
          testo: "Chi siamo",
          active: false
        },
        {
          testo: "Contatti",
          active: false
        }
      ]
    }
  }
}

</script>

<style lang="scss">
  @import '../style/variables';
  .selected{
    background-color: $bgazzurro;
  }
</style>
