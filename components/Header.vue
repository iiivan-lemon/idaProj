<template>
  <div :class="$style.header">
    <span :class="$style.title">Добавление товара</span>
    <div :class="$style.filter">По умолчанию
      <svg :class="$style.arrowFilter" width="8" height="6" viewBox="0 0 8 6" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M7.48532 1.24264L4.24268 4.48528L1.00003 1.24264" stroke="#B4B4B4"/>
      </svg>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header"
}
</script>

<style module lang="scss">

.filter{
  padding: 10px 28px 11px 16px;
  font-style: normal;
  font-weight: 400;
  font-size: 12px;
  line-height: 15px;
  color: #B4B4B4;
  background: #FFFEFB;
  box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
  border-radius: 4px;
}

.header{
  display: flex;
  margin-top: 32px;
  margin-left: 32px;
  margin-right: 32px;
  justify-content: space-between;
  align-items: center;
}

.title{
  font-style: normal;
  font-weight: 600;
  font-size: 28px;
  line-height: 35px;
  color: #3F3F3F;
  display: block;
}
.arrowFilter{
  cursor: pointer;
}
</style>

