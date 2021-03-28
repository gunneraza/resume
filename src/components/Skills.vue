<template>
  <div class="section section-skills">
    <div class="section__header">
      <div class="section__title title-1">Расскажите о себе чекбоксами</div>
      <div class="section__subtitle">Отметьте чекбоксами пункты, которые соответствуют вашим скиллам. (пункт/пункт/пункт - пункты в которых несколько технологий, оставьте только те которыми владеете)</div>
    </div>
    <div class="section__body">
      <div class="skills">
        <div class="skill" v-for="skill in skills" :key="skill.label" :class="{ active: skill.checked}">
          <div class="skill__body">
            <div class="skill__box">
              <div class="skill__check"></div>
            </div>
            <div class="skill__title">{{ skill.label}}</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import { defineComponent } from 'vue'

  export default defineComponent({
    name: 'Skills',
    setup() {
      let skills = [
        {
          label: 'БЭМ/OOCSS',
          checked: true,
        },
        {
          label: 'Pug (Jade)',
          checked: false
        },
        {
          label: 'Stylus/LESS/SASS',
          checked: true
        },
        {
          label: 'Работаю с SVG',
          checked: true
        },
        {
          label: 'Верстаю семантично',
          checked: true
        },
        {
          label: 'Accessibility (A11Y)',
          checked: false
        },
        {
          label: 'ES2015/ES2016',
          checked: true
        },
        {
          label: 'Gulp/GRUNT',
          checked: false
        },
        {
          label: 'Webpack',
          checked: true
        },
        {
          label: 'Дружу с WebGL',
          checked: false
        },
        {
          label: 'jQuery',
          checked: true
        },
        {
          label: 'Знаю/изучаю VueJs',
          checked: true
        },
        {
          label: 'Знаю/изучаю React',
          checked: false
        },
        {
          label: 'Знаю/изучаю Node.js',
          checked: true
        },
        {
          label: 'Ajax',
          checked: true
        },
        {
          label: 'Я знаю Wordpress',
          checked: true
        },
        {
          label: 'Я знаю laravel',
          checked: true
        },
        {
          label: 'Верстаю Pixel perfect',
          checked: true
        },
        {
          label: 'Всегда в сети онлайн',
          checked: true
        },
        {
          label: 'Я пунктуалкен',
          checked: true
        },
        {
          label: 'Я ленивый(-ая)',
          checked: false
        }
      ]
      return {
        skills
      }
    },
  })
</script>

<style lang="scss">
  .skills {
    display: flex;
    flex-flow: row wrap;
    margin-left: -10px;
    margin-right: -15%;
  }

  .skill {
    flex: 0 0;
    flex-basis: calc(33.333333% - 20px);
    margin: 0 10px 20px 10px;


    &__body {
      display: flex;
      align-items: center;
      cursor: pointer;
    }


    &__box {
      background-image: url('./box.png');
      background-repeat: no-repeat;
      background-position: center center;
      background-size: contain;
      width: 20px;
      height: 20px;
      margin-right: 10px;
      position: relative;
    }

    &__check {
      background-image: url('./check.png');
      background-repeat: no-repeat;
      background-position: center center;
      background-size: contain;
      width: 28px;
      height: 28px;
      position: absolute;
      top: -10px;
      display: none;
    }

    &__title {
      font-size: 26px;
      font-weight: 700;
    }
  }

  .skill.active {
    .skill__check {
      display: block;
    }
  }
</style>
