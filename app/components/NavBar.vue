<template lang="">
  <nav class="nav">
    <div>
      <a href="/">
        <img class="nav__logo" src="/imgs/traux.png"></img>
      </a>
    </div>
    <div class="d-flex flex-column justify-start nav__hamburger d-lg-none d-xl-none d-xxl-none" @click="handleClick">
      <v-icon icon="mdi-menu d-md-none"></v-icon>
    </div>
    <div class="justify-space-around flex-row w-50 d-sm-none d-xs-none d-md-flex d-lg-flex">
      <v-list v-if="showMenu" key="page"> 
        <v-list-item-title v-for="page in pages" :key="page">{{ page }}</v-list-item-title>
      </v-list>
    </div>
  </nav>
</template>
<script setup>
const showMenu = ref(false);
const handleClick = () => {
  showMenu.value = !showMenu.value;
}
const pages = ["Product design", "Content design", "About", "Contact" ]
</script>
<style lang="scss">
.nav {
  display: flex;
  justify-content: space-between;
  z-index: 2;
  width: 100%;
  box-sizing: border-box;
  padding-bottom: 1vw;
  background-color: #fff;
  padding-right: 4vw;
  border-bottom: 1px solid #fbaf17;
  &__logo {
    height: 30px;
  }
}
</style>