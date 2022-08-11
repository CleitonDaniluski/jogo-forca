<template>
    <div class="teclado">
        
        <button class="teclado-botao" 
        v-for="(letra, key) in 'abcdefghijklmnopqrstuvwxyz'"
        :key="key"
        :disabled="verificarLetra(letra)"
        v-on:click="jogar(letra)"
        >
        {{letra}}
        </button>

    </div>
</template>


<script>
export default{
    name: 'teclado',
    props:{
      letras: Array,
      verificarLetra: Function,
      jogar: Function
    },
    data(){
        return {
           
        }
    },
    methods:{
        
    },
    components:{
        
    }
}
</script>


<style>
.teclado{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    max-width: 80%;
    margin-top: 20px;
    }

.teclado-botao{
    margin: 8px;
    text-transform: uppercase;
}
</style>