<template>
    <div class="final">
        
       <div :class="`final-texto ${etapa}`">
           {{texto}}
       </div>

       <button class="final-botao"
        v-on:click="jogarNovamente"> Jogar Novamente</button>

    </div>
</template>


<script>
export default{
    name: 'final',
    props:{
        etapa: String,
        texto: String,
        jogarNovamente: Function
     
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

.final-texto{
    margin: 20px 0px;
    font-size: 24px;
    font-weight: bold;
    align-content: center;
    align-items: center;
}

.final-texto.enforcado{
    color:#c0392b
}

.final-texto.ganhador{
    color:#2ecc71;
}

.final-botao{
    font-weight: bold;
    text-transform: uppercase;
}

</style>