<template>
  <div class="section section-about">
    <div class="section__header">
      <div class="section__title title-1">Расскажите о себе словами</div>
      <div class="section__subtitle">Напишите пару предложений, чем вас привлекла наша вакансия и чего вы ожидаете от
        работы в Creativemade.ru Кстати, будет здорово, если при нехватке места для текста строки будут добавляться
        автоматически.
      </div>
    </div>
    <div class="section__body">
      <div class="about">
        <div class="about__field">
          <textarea class="textarea" rows="2" @keypress="resize">Хотелось бы присоединиться к вашей команде, научится чему то большему у ваших опытных разработчиков, и стать частью одной большой команды.</textarea>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import {defineComponent, ref} from 'vue'

export default defineComponent({
  name: 'About',
  methods: {
    resize() {
      setTimeout(() => {
        let field = document.querySelector('.textarea')
        field.style.cssText = 'height:auto; padding:0'
        field.style.cssText = 'height:' + field.scrollHeight + 'px';
      }, 0)
    }
  },
})
</script>

<style lang="scss">
.about {
  &__field {
    textarea {
      background: transparent;
      border: 0;
      border-bottom: 2px solid #2f1b15;
      outline: none;
      resize: none;
      font-size: 30px;
      width: 100%;
      height: auto;
    }
  }
}
</style>
