<template>
    <div class="app">
      <h1>単一計算</h1>
      <h2>{{table_named1}}</h2>
      <table class="select_tbl" border="1">
        <thead>
          <tr>
            <th>数値1</th>
            <th>数値2</th>
            <th>記号</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>
              <input v-model="atai1" type="number" min="1"/>
            </td>
            <td>
              <input v-model="atai2" type="number" min="1"/>
            </td>
            <td>
              <select v-model="types">
                <option disabled value="">prease typed</option>
                <option>+</option>
                <option>-</option>
                <option>*</option>
                <option>/</option>
              </select>
            </td>
          </tr>
        </tbody>
      </table>
      <h2>計算結果</h2>
      <div v-if="types != ''">
        <p class="success_data">上記に入力された内容が計算されます</p>
        <table border="1" class="ans_tbl">
          <thead>
            <tr>
              <th>計算値１</th>
              <th>記号</th>
              <th>計算値２</th>
              <th>=</th>
              <th>値</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>{{atai1}}</td>
              <td>{{types}}</td>
              <td>{{atai2}}</td>
              <td>=</td>
              <td v-if="types==='+'">{{parseInt(atai1)+parseInt(atai2)}}</td>
              <td v-else-if="types==='-'">{{parseInt(atai1)-parseInt(atai2)}}</td>
              <td v-else-if="types==='*'">{{(parseFloat(atai1).toFixed(2))*(parseFloat(atai2).toFixed(2))}}</td>
              <td v-else-if="types==='/'">{{(parseFloat(atai1).toFixed(2))/(parseFloat(atai2).toFixed(2))}}</td>
            </tr>
          </tbody>
        </table>
      </div>
      <div v-else-if="types === ''">
        <p class="none_data">{{table_named1}}に入力されたデータが不正か入力漏れがあります<br/>再入力してください</p>
      </div>
    </div>
</template>

<script>
    export default {
        name: "only_calc",
        data(){
          return{
            msg:'test',
            atai1:1,
            atai2:1,
            types:'',
            table_named1:'計算用数値入力テーブル'

          }
        }
    }
</script>

<style scoped>
h1{
  color: #000000;
  text-align: center;
}
h2{
  color: #000000;
  text-align: center;
}
.none_data{
  text-align: center;
  color: red;
  font-weight: bold;
}
.success_data{
  text-align: center;
  color: darkcyan;
  font-weight: lighter;
}
.select_tbl{
  text-align: center;
  margin: auto;
}
.ans_tbl{
  text-align: center;
  margin: auto;
}
</style>
