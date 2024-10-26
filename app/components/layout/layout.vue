<template>
  <div>
    <header>
      <nav-bar></nav-bar>
    </header>
    <hr />
    <main>
      <slot name="content"></slot>
    </main>
  </div>
</template>
<script>
export default {
  name: 'LayoutWrapper',
}
</script>
<style lang="">
    
</style>