<template>
  <div :class="$style.menu">
    <div :class="$style.elMenu" v-for="item in list">
      <div>
        <span :class="$style.titleInput" v-text="item.title"></span>
        <svg v-if="item.important" :class="$style.importantInput" width="4" height="4" viewBox="0 0 4 4" fill="none"
             xmlns="http://www.w3.org/2000/svg">
          <rect width="4" height="4" rx="2" fill="#FF8484"/>
        </svg>
      </div>
      <input v-if="item.important" :class="$style.inputItem__normal" :placeholder="item.placeholder" type="text"
             required>
      <textarea v-else rows="2" cols="15"  :class="$style.inputItem__descr" :placeholder="item.placeholder" type="text" required>
      </textarea>
    </div>
    <button :class="$style.btnMenu">Добавить товар</button>
  </div>
</template>

<script>
export default {
  name: "Menu",
  data() {
    return {
      list: [
        {
          title: "Наименование товара",
          placeholder: "Введите наименование товара",
          important: true
        },
        {
          title: "Описание товара",
          placeholder: "Введите описание товара",
          important: false
        },
        {
          title: "Ссылка на изображение товара",
          placeholder: "Введите ссылку",
          important: true
        },
        {
          title: "Цена товара",
          placeholder: "Введите цену",
          important: true
        }]
    }
  },
  mounted() {

  }
}
</script>

<style module lang="scss">
.titleInput {
  z-index: 3;
  display: inline-block;
  width: fit-content;
}

.importantInput {
  z-index: 3;
  margin-bottom: 10px;
}

.elMenu {
  z-index: 3;
  margin-bottom: 16px;
  row-gap: 4px;
  display: flex;
  flex-direction: column;
}

.menu {
  z-index: 2;
  position: sticky;
  height: fit-content;
  background: #FFFEFB;
  box-shadow: 0px 20px 30px rgb(0 0 0 / 4%), 0px 6px 10px rgb(0 0 0 / 2%);
  border-radius: 4px;
  display: flex;
  width: 332px;
  flex-direction: column;
  padding: 41px 24px 24px 24px;
  top: 24px;

}


.inputItem__normal {
  z-index: 5;
  font-family: sans-serif;
  font-style: normal;
  font-weight: 400;
  padding-left: 16px;
  width: 284px;
  height: 36px;
  background: #FFFEFB;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  border-radius: 4px;
  border: transparent;

  &::placeholder {
    font-family: sans-serif;
    font-style: normal;
    font-weight: 400;
      padding-left: 16px;
  }
}

.inputItem__descr {
  z-index: 5;
  font-family: sans-serif;
  font-style: normal;
  font-weight: 400;
  padding-left: 16px;
resize: none;
  width: 284px;
  height: 108px;
  background: #FFFEFB;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  border-radius: 4px;
  border: transparent;
  &::placeholder {
    font-family: sans-serif;
    font-style: normal;
    font-weight: 400;
    padding-left: 16px;
  }
}


.btnMenu {
  cursor: pointer;
  border: transparent;
  background: #EEEEEE;
  border-radius: 10px;
  color: #B4B4B4;
  font-weight: 600;
  font-size: 12px;
  line-height: 15px;
  padding-block: 10px;
  text-align: center;
  letter-spacing: -0.02em;
  transition: all 0.2s ease;

  &:active {
    transform: scale(0.9);
  }
}

</style>
