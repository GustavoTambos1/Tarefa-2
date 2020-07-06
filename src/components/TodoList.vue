<template>
  <div id="todoList">
      <div class="tarefasCaixas" v-for="(todoList, index) in tarefas" :key="index">
        {{todoList.descricao}}
      </div>
  </div>
</template>

<script>
export default {
    name:"TodoList",
    props:['tarefas']
}
</script>

<style>
    #todoList{
        background-color: grey;
        width: 600px;
        height: 200px;
        margin: 10px 0px 0px 35%;
        display: flex;
        flex-wrap: wrap;
        overflow: auto;
        border: black 1px solid;
        border-radius: 20px;
    }

    .tarefasCaixas{
        width: (tarefas);
        background-color: green;
        height: 50px;
        border: 2px solid black;
        margin: 5px 20px 0 10px;
        text-align: center;
        line-height: 50px;
        cursor: pointer;
        color: white; 
        overflow: hidden;
    }
</style>