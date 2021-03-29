<template>
  <div class="form">
    <form-input v-for="item in inputs" v-model="item.val" :key="item.label" :data="item"/>
  </div>
</template>

<script>
  import { defineComponent } from 'vue'
  import FormInput from './FormInput.vue'

  export default defineComponent({
    name: 'mainForm',
    components: { FormInput },
    setup() {
      let inputs = [
        {
          label: 'Полное ФИО',
          val: 'Забирдинов Азамат Таджалиевич'
        },
        {
          label: 'Год рождения',
          val: '1995'
        },
        {
          label: 'Место жительства',
          val: 'г.Чирчик, Узбекистан'
        },
        {
          label: 'Телефон/Телеграм',
          val: '+998 99 402-95-07'
        },
        {
          label: 'Почта',
          val: 'gunnera3a@gmail.com'
        }
      ]
      return {
        inputs
      }
    }
  })

</script>
