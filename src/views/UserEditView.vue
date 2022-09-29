<template>
  <div>
    <pre>
      {{ $route.query.page}}
      Usuário <br>

      <button @click="login()">
        Login
      </button>
    </pre>
  </div>
</template>

<script>
  export default {
    created() {
      //console.log(this.$route); route é objeto da rota atual
      console.log(this.$router); //router são as funcionalidades do esquema de roteamento.
    },
    methods: {
      login() {
        //ajax login
        this.$router.push({name: 'about'}) //push é para decidir onde levar o usuário
        console.log('chegou');
      }
    }
  }
</script>