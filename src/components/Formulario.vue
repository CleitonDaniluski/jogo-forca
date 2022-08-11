<template>
    <div class="formulario">

        <div class="formulario-title">{{title}}</div>

        <input type="text" class="formulario-input" v-model="valor">

        <button class="botao-proximo"
        :disabled="valor.length === 0"
        v-on:click="onSubmit"
        >{{button}}</button>
        

    </div>
</template>


<script>
export default{
    name: 'Formulario',
    props:{
        title: String,
        button: String,
        action: Function,
    },
    data(){
        return {
            valor:''
        }
    },
    methods:{
        onSubmit: function(){
            this.action(this.valor);
            this.valor='';
        }
    }
}
</script>


<style>
    .formulario{
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
        justify-content: center;
        margin-top: 10px;
        
    }
    
    .formulario-title{
        font-weight: bold;
        text-transform: uppercase;
        margin: 15px;

    }

    .formulario-input{
        padding: 10px 20px;
        border: 0;
        border-radius: 5px;
        margin: 10px 0px;
        text-align: center;
        color:var(--color-text-dark);
        font-size: 16px;
        font-weight: bold;
        text-transform: uppercase;
        
    }

    .botao-proximo{
        text-transform: uppercase;
        font-weight: bold;
        }
</style>