<template>
  <div class="form-input">
    <div class="form-input__label title-2">{{ data.label }}</div>
    <div class="form-input__field">
      <div class="input">
        <input type="text" :value="data.val">
      </div>
    </div>
  </div>
</template>

<script>
  import { defineComponent } from 'vue'

  export default defineComponent({
    name: 'FormInput',
    props: {
      data: Object
    },
    setup(props) {
      const data = props.data

      return {
        data,
      }
    }
  })
</script>

<style lang="scss">
  .form-input {
    display: flex;
    align-items: flex-end;
    padding: 10px 0;

    &__label {
      white-space: nowrap;
      padding-right: 20px;
    }

    &__field {
      width: 100%;
    }
  }

  .input {
    display: block;
    width: 100%;

    input {
      width: 100%;
      background: transparent;
      border: 0;
      border-bottom: 2px solid #2f1b15;
      outline: none;
      font-size: 38px;
      font-family: 'Courier New', monospace;
    }
  }
</style>
