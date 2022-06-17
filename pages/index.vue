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
import Header from "~/components/Header.vue";

export default Vue.extend({
  name: 'IndexPage',
  components: {Header},
})
</script>
<style module lang="scss">
body{
  background: #E5E5E5;
}

.main{
  margin-top: 16px;
  margin-left: 32px;
  margin-right: 32px;
  display: flex;
  flex-direction: row;
}
.items{
  grid-column-gap: 16px;
  margin-left: 16px;
  display: inline-grid;
  grid-template-columns: 1fr 1fr 1fr;
}

</style>

