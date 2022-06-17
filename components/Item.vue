<template>
  <div :class="$style.item">
    <img :class="$style.itemImg" src="../static/wall.png" alt="no pic">
    <div :class="$style.itemDescr">
      <span :class="$style.itemTitle">FFGFGFGF</span>
      <span :class="$style.itemInfo">fsefsefsefsefsefsefsefsefsefsfesefsefsef</span>
      <span :class="$style.itemPrice">123123124</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "Item"
}
</script>

<style module lang="scss">

.item {
  cursor: pointer;
  display: flex;
  background: #FFFEFB;
  box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.04), 0px 6px 10px rgba(0, 0, 0, 0.02);
  border-radius: 4px;
  flex-direction: column;
  height: fit-content;
  margin-bottom: 16px;
  transition: all 0.25s ease;
  &:active{
    transform: scale(0.98);
  }
}
.itemImg{
  width: 322px;
  height: 200px;
}
.itemDescr{
  padding-inline: 16px;
  display: flex;
  flex-direction: column;
}
.itemTitle{
  margin-block: 16px;
  font-style: normal;
  font-weight: 600;
  font-size: 20px;
  line-height: 25px;
  color: #3F3F3F;
}
.itemInfo{
  margin-bottom: 32px;
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 20px;
  color: #3F3F3F;
}
.itemPrice{
  margin-bottom: 24px;
  font-style: normal;
  font-weight: 600;
  font-size: 24px;
  line-height: 30px;
  color: #3F3F3F;
}

</style>
