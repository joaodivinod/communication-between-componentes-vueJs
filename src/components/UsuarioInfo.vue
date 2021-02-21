<template>
    <div class="componente">
        <h2>As Informações de Usuário</h2>
        <p>Vários detalhes...</p>
        <p>Nome do Usuario : <strong>{{ nome }}</strong></p>
      <button @click="reiniarNome()">Reinicializar Nome</button>
      <p>idade :<strong> {{idade}}</strong></p>

    </div>
</template>

<script>
export default {
    props:{
      nome:{
        type:String,
        default:'Anônimo',
      },
      idade:{
        type:Number,

      }
    },
    methods:{
      inverterNome(){
       return  this.nome.split('').reverse().join('')
      },
      reiniarNome(){
        this.nome = 'João Divino'

      }
    }
}
</script>

<style scoped>
    .componente {
        flex: 1;
        background-color: #ec485f;
        color: #fff;
    }
</style>
