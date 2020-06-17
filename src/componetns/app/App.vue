<template>
  <div class="app-box">
    <div id="app">
      <h1 class="h1">{{h1}}</h1>
      <div class="control">
        <buttons></buttons>
        <search></search>
      </div>
      <list-s></list-s>
    </div>
  </div>
</template>
<script>
    import lists from "../lists/lists.vue";
    import buttons from "../buttons/buttons.vue";
    import search from "../search/search.vue";
    export default {
        data() {
            return {
                h1: 'Курсы валют',
            }
        },
        components: {
            listS: lists,
            buttons: buttons,
            search:search,
        }
    }
</script>
<style lang="scss">
  @import 'app.scss';
</style>
