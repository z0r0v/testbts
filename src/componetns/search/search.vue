<template>
  <div class="control--search">
    <label>{{text}} <input type="text"></label>
  </div>

</template>
<script>
    export default {
        name: "search",
        data() {
            return {
                text: 'Поиск',
            }
        },
    }
</script>

<style lang="scss">
  @import 'search.scss';
</style>

