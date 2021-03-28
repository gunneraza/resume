<template>
  <div class="container">
    <div class="header">
      <div class="header__title" style="background-image: url('./delo.png')"></div>
      <div class="header__img" style="background-image: url('./secret.png')"></div>
    </div>
    <main-form/>
  </div>
</template>

<script>
  import { defineComponent } from 'vue'
  import MainForm from './components/MainForm.vue'

  export default defineComponent({
    name: 'App',
    components: { MainForm },
  })
</script>

<style lang="scss">
@import url('https://allfont.ru/allfont.css?fonts=courier-new');
@import url('https://fonts.googleapis.com/css2?family=PT+Sans:wght@400;700&display=swap');

  body {
    background-image: url("./background.png");
    color: #2f1b15;
    font-family: 'PT Sans', sans-serif;
  }

  .container {
    max-width: 1240px;
    margin: 0 auto;
    padding: 0 20px;
  }

  .header {
    padding-top: 200px;
    padding-bottom: 100px;
    position: relative;

    &__title {
      height: 250px;
      width: 300px;
      margin: 0 auto;
      background-repeat: no-repeat;
      background-size: contain;
      background-position: center center;
    }

    &__img {
      width: 350px;
      height: 200px;
      background-repeat: no-repeat;
      background-size: contain;
      background-position: center center;
      position: absolute;
      top: 160px;
      right: 0;
    }
  }

  .title-2 {
    font-size: 30px;
    font-weight: 700;
  }
</style>
