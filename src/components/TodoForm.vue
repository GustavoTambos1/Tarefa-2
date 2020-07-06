<template>
  <div id="Form">
  <input id="texto" type="text" placeholder="Nova Tarefa?" v-model="novaTarefa">
  <button id="botao" @click="adicionarTarefa">OK</button>
  </div>
</template>

<script>
export default {
    name: "TodoForm",
    data: function(){
        return{
            novaTarefa: ''
        }
    }, methods:{
        adicionarTarefa: function(){
            this.$emit('addTarefa',{novaTarefa: this.novaTarefa})
        }
    }
}
</script>

<style>
    #Form{
        background-color: grey;
        width: 600px;
        height: 200px;
        margin: 80px 0px 0px 35%;
        border: 1px black solid;
        border-radius: 20px;
    }

    #texto{
        margin: 80px 0 0 27%;
        height: 20px;
        width: 200px;
        border: black 1px solid;
    }

    #botao{
       width: 50px;
       height: 20px;
       color: green;
       outline: none;
       cursor: pointer;
       margin: 0px 5px;
    }
</style>