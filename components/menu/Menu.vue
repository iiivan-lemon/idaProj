<template>
  <div :class="$style.menu">
    <form id="form">
      <div :class="$style.elMenu" v-for="item in list">
        <div>
          <span :class="$style.titleInput" v-text="item.title"></span>
          <svg v-if="item.important" :class="$style.importantInput" width="4" height="4" viewBox="0 0 4 4" fill="none"
               xmlns="http://www.w3.org/2000/svg">
            <rect width="4" height="4" rx="2" fill="#FF8484"/>
          </svg>
        </div>
        <input :name="item.key" v-if="item.important"  :class="$style.inputItem__normal" :placeholder="item.placeholder" type="text"
               required>
        <textarea :name="item.key"  v-else rows="2" cols="15"  :class="$style.inputItem__descr" :placeholder="item.placeholder" type="text" required>
        </textarea>
      </div>
      <button :class="$style.btnMenu">Добавить товар</button>
    </form>

  </div>
</template>

<script>

export default {
  name: "Menu",
  data() {
    return {
      list: [
        {
          key: "title",
          title: "Наименование товара",
          placeholder: "Введите наименование товара",
          important: true
        },
        {
          key: "descr",
          title: "Описание товара",
          placeholder: "Введите описание товара",
          important: false
        },
        {
          key: "imghref",
          title: "Ссылка на изображение товара",
          placeholder: "Введите ссылку",
          important: true
        },
        {
          key: "price",
          title: "Цена товара",
          placeholder: "Введите цену",
          important: true
        }]
    }
  }
}
</script>

<style module lang="scss">
@import "./menu";
</style>
