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
@import "./header";
</style>

