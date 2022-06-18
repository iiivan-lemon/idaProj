<template>
  <root>
    <Header/>
    <div :class ="$style.main">
      <Menu/>
      <div :class ="$style.items">
        <Item v-for="i in 14"/>
      </div>
      <div></div>
    </div>
  </root>
</template>

<script lang="ts">
import Vue from 'vue'
// import Header from "~/components/header/Header.vue";

export default Vue.extend({
  name: 'IndexPage',
  // components: {Header},
})
</script>

<style module lang="scss">
@import "index";
</style>

