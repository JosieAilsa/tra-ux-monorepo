<template lang="">
  <div class="nav-header w-100">
    <div class="nav-bar w-100">
      <div>
        <a href="/">
          <img class="nav-bar__logo" src="/imgs/traux.png"></img>
        </a>
      </div>
      <div class="d-flex flex-column justify-start nav__hamburger d-lg-none d-xl-none d-xxl-none" @click="handleClick">
        <v-icon icon="mdi-menu d-md-none"></v-icon>
      </div>
      <nav class="d-flex justify-space-around flex-row d-sm-none d-md-none d-lg-flex nav__list">
        <v-list v-if="showMenu" key="page" class="d-flex flex-row justify-space-around w-100">
          <v-list-item-title v-for="(page, i) in pages" :key="page" class="ml-2 mr-2 d-flex flex-row align-center">
            <a :href="`/${tag[i]}`" class="text-decoration-none"> {{ page }} </a>
          </v-list-item-title>
        </v-list>
      </nav>
    </div>
  </div>
</template>
<script setup>
const showMenu = ref(true)
const handleClick = () => {
  showMenu.value = !showMenu.value
}
const pages = ['Product design', 'Content design', 'About', 'Contact']
const tag = ['product', 'content', 'about', 'contact']
</script>
<style lang="scss">
.nav-header {
  padding-top: 1vw;
  padding-bottom: 1vw;
  padding-left: 4vw;
  padding-right: 4vw;
  border-bottom: 4px solid #fbaf17;
  .nav-bar {
    display: flex;
    justify-content: space-between;
    z-index: 2;
    width: 100%;
    box-sizing: border-box;
    padding-bottom: 1vw;
    background-color: #fff;
    &__logo {
      width: auto;
      max-width: 100%;
      max-height: 61px;
    }
    &__list {
      a {
        text-decoration: none;
      }
      @media screen and (min-width: 0px) {
        display: none;
      }
      @media screen and (min-width: 1280px) {
        display: flex;
      }
    }
  }
}
</style>