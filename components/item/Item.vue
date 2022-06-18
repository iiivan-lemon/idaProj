<template>
  <div :class="$style.item">
    <img :class="$style.itemImg" src="../../static/wall.png" alt="no pic">
    <div :class="$style.itemDescr">
      <span :class="$style.itemTitle">TITLE ITEM</span>
      <span :class="$style.itemInfo">Lorem ipsum dolor sit amet. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</span>
      <span :class="$style.itemPrice">12312 $</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "Item"
}
</script>

<style module lang="scss">
@import "./item";
</style>
