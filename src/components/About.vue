<template>
  <div class="section section-about">
    <div class="section__header">
      <div class="section__title title-1">Расскажите о себе словами</div>
      <div class="section__subtitle">Напишите пару предложений, чем вас привлекла наша вакансия и чего вы ожидаете от работы в Creativemade.ru Кстати, будет здорово, если при нехватке места для текста строки будут добавляться автоматически.</div>
    </div>
    <div class="section__body">
      <div class="about">
        <div class="about__field">
          <div class="input">
            <input type="text">
          </div>
        </div>
        <div class="about__field">
          <div class="input">
            <input type="text">
          </div>
        </div>
        <div class="about__field">
          <div class="input">
            <input type="text">
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'About'
})
</script>

<style lang="scss">
  .about {
    &__field {
      margin-bottom: 20px;
    }
  }
</style>
