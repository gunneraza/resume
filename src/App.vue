<template>
  <div class="container">
    <div class="header">
      <div class="header__title" style="background-image: url('./delo.png')"></div>
      <div class="header__img" style="background-image: url('./secret.png')"></div>
    </div>
    <about/>
    <future/>
    <div class="section">
      <div class="date">
        <div class="date__title">Дата nadsadx</div>
        <div class="input">
          <input type="text" :value="date">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import { defineComponent } from 'vue'
  import MainForm from './components/MainForm.vue'
  import Skills from './components/Skills.vue'
  import JsLvl from './components/JsLvl.vue'
  import About from './components/About.vue'
  import Future from './components/Future.vue'

  export default defineComponent({
    name: 'App',
    components: { MainForm, Skills, JsLvl, About, Future },
    setup() {
      let date = '29.03.2021'

      return {
        date
      }
    }
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

      @media (max-width: 1200px) {
        top: 90px;
        width: 300px;
      }

      @media (max-width: 1024px) {
        top: 50px;
        width: 280px;
      }
    }
  }

  .date {
    display: flex;
    align-items: flex-end;
    width: 500px;
    padding-bottom: 100px;

    @media (max-width: 768px) {
      width: 100%
    }

    &__title {
      font-size: 24px;
      font-weight: 700;
      white-space: nowrap;
      margin-right: 20px;
    }
  }

  .title-2 {
    font-size: 30px;
    font-weight: 700;

    @media (max-width: 1024px) {
      font-size: 26px;
    }
  }

  .title-1 {
    font-size: 34px;
    font-weight: 700;
  }

  .section {
    padding-top: 100px;

    &__title {
      margin-bottom: 10px;
    }

    &__subtitle {
      font-size: 18px;
      color: #3d3d3d;
    }

    &__body {
      margin-top: 40px;
    }
  }
</style>
