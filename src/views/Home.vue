<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
  <div id="app">
    <p>Novo curso:
      <input type="text" v-model="novo">
      <button @click="incluir">Inserir</button>
    </p>
    <ul>
      <li v-for=" (curso, indice) in cursos" @click="excluir(indice)" :key="indice">
        {{curso.nome}}
      </li>
    </ul>  
  </div>  
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  }
}
</script>
