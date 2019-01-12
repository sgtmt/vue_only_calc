<template>
    <div class="app">
      <h1>単一計算</h1>
      <p>{{msg}}</p>
    </div>
</template>

<script>
    export default {
        name: "only_calc",
        data(){
          return{
            msg:'test'
          }
        }
    }
</script>

<style scoped>
h1{
  color: #000000;
  text-align: center;
}
</style>
