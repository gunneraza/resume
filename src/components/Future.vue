<template>
  <div class="section section-future">
    <div class="section__header">
      <div class="section__title title-1">Какие у вас планы на будущее?</div>
      <div class="section__subtitle">Этот ответ ни на что не повлияет. Не беда, если в будущем ваши планы поменяются.</div>
    </div>
    <div class="section__body">
      <div class="future-radio">
        <div class="future-radio__item active">
          <div class="future-radio__circle">
            <div class="future-radio__dot"></div>
          </div>
          <div class="future-radio__title">Верстать</div>
        </div>
        <div class="future-radio__item">
          <div class="future-radio__circle">
            <div class="future-radio__dot"></div>
          </div>
          <div class="future-radio__title">Прокачиваться в JS</div>
        </div>
        <div class="future-radio__item">
          <div class="future-radio__circle">
            <div class="future-radio__dot"></div>
          </div>
          <div class="future-radio__title">Менеджерство</div>
        </div>
        <div class="future-radio__item">
          <div class="future-radio__circle">
            <div class="future-radio__dot"></div>
          </div>
          <div class="future-radio__title">Другое</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'Future'
})
</script>

<style lang="scss">
    .future-radio {
      display: flex;

      &__item {
        display: flex;
        align-items: center;
        cursor: pointer;
        margin-right: 30px;
      }

      &__item.active {
        .future-radio__dot {
          display: block;
        }
      }

      &__dot {
        background-image: url('./dot.png');
        background-position: center center;
        background-size: contain;
        background-repeat: no-repeat;
        width: 16px;
        height: 16px;
        display: none;
      }

      &__circle {
        background-image: url('./circle.png');
        background-position: center center;
        background-size: contain;
        background-repeat: no-repeat;
        width: 26px;
        height: 26px;
        margin-right: 10px;
        display: flex;
        align-items: center;
        justify-content: center;
      }

      &__title {
        font-size: 24px;
        font-weight: 700;
      }
    }
</style>
