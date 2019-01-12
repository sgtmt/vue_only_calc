<template>
    <div class="app">
      <h1>単一計算</h1>
      <h2>計算用数値入力テーブル</h2>
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
            types:''

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
.select_tbl{
  text-align: center;
  margin: auto;
}
</style>
