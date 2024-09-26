<template lang="">
  <div class="nav">
      <div>
          <a href="/">
            <img class="nav__logo" src="/imgs/traux.png"></img>
          </a>
      </div>
      <div class="d-flex flex-column justify-start nav__hamburger d-md-none" @click="handleClick">
        <v-icon icon="mdi-menu d-md-none"></v-icon>
      </div>
  </div>
</template>
<script setup>
const showMenu = ref(false);
const handleClick = () => {
  showMenu.value = !showMenu.value;
}
</script>
<style lang="scss">
.nav {
  display: flex;
  justify-content: space-between;
  z-index: 2;
  width: 100%;
  box-sizing: border-box;
  padding-bottom: 1vw;
  padding-left: 4vw;
  background-color: #fff;
  padding-right: 4vw;
  border-bottom: 1px solid #fbaf17;
  &__logo {
    height: 30px;
  }
}
</style>