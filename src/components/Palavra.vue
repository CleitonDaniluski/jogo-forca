<template>
    <div class="palavra">
        
        <div class="palavra-letras">

            <div class="palavra-letra" v-for="(letra,key) in palavra" :key="key">
                {{ (verificarLetra(letra) || etapa === 'enforcado')? letra : '' }}
            </div>

        </div>

        <div class="palavra-dica">
            {{dica}}
        </div>

    </div>
</template>


<script>
export default{
    name: 'Palavra',
    props:{
      palavra: String,
      dica: String,
      verificarLetra: Function,
      etapa: String
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

.palavra{
    text-transform: uppercase;
    display: flex;
    flex-direction: column;
    text-align: center;
    align-items: center;
}

.palavra-letras{
    display: flex;
    margin-bottom: 20px;
}

.palavra-letra{
    width: 50px;
    height: 50px;
    margin: 0px 5px;
    border-bottom: 1px solid #ecf0f1;
    display: flex;
    justify-content: center;
    align-items: center;
    font-weight: bold;
    text-transform: uppercase;
}

.palavra-dica{
    text-transform: uppercase;
    font-weight: bold;
}

</style>