<template>
  <div class="control--box">
    <div class="control--box__button add">
      <button></button><span>{{firstButton}}</span>
    </div>
    <div class="control--box__button update">
      <button></button><span>{{secondButton}}</span>
    </div>
  </div>
</template>
<script>
    export default {
        data() {
            return {
                firstButton: 'Добавить',
                secondButton: 'Обновить данные',
            }
        }
    }
</script>
<style lang="scss">
  @import 'buttons.scss';
</style>
