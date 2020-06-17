<template>
  <div>
    <table class="table">
      <thead>
      <tr>
        <th>Номер строки</th>
        <th>Буквенный код валюты</th>
        <th>Наименование валюты</th>
        <th>Количество единиц валюты</th>
        <th>Курс к бел. рублю</th>
      </tr>
      </thead>
      <!--      это должно формироваться автоматом из полученных данных-->
      <tbody>
      <tr>
        <th>1</th>
        <td>RU</td>
        <td>Российский рубль</td>
        <td>100</td>
        <td>3.4020</td>
        <td>
          <button-plus></button-plus>
          <button-del></button-del>
        </td>
      </tr>
      <tr>
        <th>2</th>
        <td>RU</td>
        <td>Российский рубль</td>
        <td>100</td>
        <td>3.4020</td>
        <td>
          <button-plus></button-plus>
          <button-del></button-del>
        </td>
      </tr>
      <tr>
        <th>3</th>
        <td>RU</td>
        <td>Российский рубль</td>
        <td>100</td>
        <td>3.4020</td>
        <td>
          <button-plus></button-plus>
          <button-del></button-del>
        </td>
      </tr>
      </tbody>
      <!--      это должно формироваться автоматом из полученных данных-->
    </table>
  </div>
</template>
<script>
    import buttonPlus from "../button-plus/button-plus.vue";
    import buttonDel from "../button-del/button-del";

    export default {
        data() {
            return {
                carName: 'Ford',
                carYear: 2015,
            }
        },
        components: {
            buttonPlus: buttonPlus,
            buttonDel: buttonDel,
        }
    }
</script>
<style lang="scss">
  @import 'lists.scss';
</style>
