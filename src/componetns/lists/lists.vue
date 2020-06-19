<template>
  <div>
    <table id="table_id" class="display">
      <thead>
      <tr>
        <th>{{numberCurrency}}</th>
        <th>{{codСurrency}}</th>
        <th>{{nameСurrency}}</th>
        <th>{{valСurrency}}</th>
        <th>{{exchangeRate}}</th>
        <th class="butttons"></th>
      </tr>
      </thead>
      <tbody>
      <tr>
        <td>Row 1 Data 1</td>
        <td>Row 1 Data 2</td>
        <td>Row 1 Data 3</td>
        <td>Row 1 Data 4</td>
        <td>Row 1 Data 5</td>
        <td>Row 1 Data 6</td>
      </tr>
      </tbody>
    </table>
    <div class="border"></div>
  </div>
</template>
<script>
    import * as $ from 'jquery';
    import * as dt from 'datatables.net';

    const url = 'https://cors-anywhere.herokuapp.com/https://www.cbr-xml-daily.ru/daily_json.js';
    const data = [];
    let i = 1;
    const buttons = "<button class='button-del'></button>" +
        "<button class='button-plus'></button>";

    const getCurses = (url) => {
        let xhr = new XMLHttpRequest();
        xhr.open('GET', url, false);
        try {
            xhr.send();
            if (xhr.status != 200) {
                alert(`Ошибка ${xhr.status}: ${xhr.statusText}`);
            } else {
                return xhr.response;
            }
        } catch (err) {
            alert("Запрос не удался");
        }
    };

    const getRandomArbitrary = (min, max) => {
        return Math.random() * (max - min) + min;
    };

    const dadaParse = JSON.parse(getCurses(url));

    $.each(dadaParse.Valute, function (index, elem) {
        let randomValue = parseInt((getRandomArbitrary(100, 800) * 100) / 100);
        data.push([
            i++,
            elem.CharCode,
            elem.Name,
            randomValue,
            elem.Value,
            buttons
        ])
    });
    $(document).ready(function () {
        $('#table_id').DataTable(
            {
                data: data,

            }
        );
    });
    export default {
        data() {
            return {
                numberCurrency: 'Номер строки',
                codСurrency: 'Буквенный код валюты',
                nameСurrency: 'Наименование валюты',
                valСurrency: "Количество единиц валюты",
                exchangeRate: "Курс к бел. рублю",
            }
        },
    }
</script>
<style lang="scss">
  @import 'lists.scss';


</style>
