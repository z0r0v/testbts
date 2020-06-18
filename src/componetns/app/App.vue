<template>
  <div class="app-box">
    <div id="app">
      <h1 class="h1">{{h1}}</h1>
      <div class="control">
        <buttons></buttons>
      </div>
      <list-s></list-s>
    </div>
  </div>
</template>
<script>
    import lists from "../lists/lists.vue";
    import buttons from "../buttons/buttons.vue";
    export default {
        data() {
            return {
                h1: 'Курсы валют',
            }
        },
        components: {
            listS: lists,
            buttons: buttons,
        }
    }
</script>
<style lang="scss">
  @import 'app.scss';
</style>
