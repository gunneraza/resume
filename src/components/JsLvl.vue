<template>
  <div class="section section-js">
    <div class="section__header">
      <div class="section__title title-1">Уровень владения JavaScript</div>
    </div>
    <div class="section__body">
      <div class="js-lvl">
        <div
            v-for="(item, index) in levels"
            :key="index"
            :class="{ active: index === selectedIndex }"
            @click="selectedIndex = index"
            class="js-lvl__item"
        >
          <div class="js-lvl__title" v-html="item"></div>
          <div class="js-lvl__triangle"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import {defineComponent, ref} from 'vue'

export default defineComponent({
  name: 'JsLvl',

  setup() {
    let levels = ref([
      'Не владею',
      'Использую готовые решения',
      'Использую готовые решения <br/> и умею их переделывать',
      'Пишу сложный JS с нуля'
    ])
    let selectedIndex = ref(3)

    return {
      levels, selectedIndex
    }
  }
})
</script>

<style lang="scss">
.js-lvl {
  width: 100%;
  border-top: 2px solid #2f1b15;
  display: flex;
  justify-content: space-between;

  &__item {
    padding: 20px 0;
    position: relative;
    font-weight: 700;
    font-size: 18px;
    cursor: pointer;

    &:after {
      display: block;
      content: '';
      position: absolute;
      top: 0px;
      width: 2px;
      height: 16px;
      background-color: #2f1b15;
    }

    &:last-child {
      &:after {
        right: 0;
      }
    }
  }

  &__triangle {
    width: 20px;
    height: 20px;
    background-image: url('./triangle.png');
    background-repeat: no-repeat;
    background-size: contain;
    background-position: center center;
    position: absolute;
    display: none;
  }

  &__item.active {
    &:not(:last-child) {
      .js-lvl__triangle {
        display: block;
        top: -24px;
        left: -10px;
      }
    }

    &:last-child {
      .js-lvl__triangle {
        display: block;
        top: -24px;
        right: -8px;
      }
    }
  }

}
</style>
