<script setup lang="ts">
import { ref } from 'vue'
import MeuComponente from './components/MeuComponente/MeuComponente.vue'

const nome = ref('')
const email = ref('')
const telefone = ref('')
const endereco = ref('')
const cpf = ref('')

const cadastro = ref({
  nome: '',
  email: '',
  telefone: '',
  endereco: '',
  cpf: ''
})

function cadastrar() {
  cadastro.value = {
    nome: nome.value,
    email: email.value,
    telefone: telefone.value,
    endereco: endereco.value,
    cpf: cpf.value
  }
}
</script>

<template>
  <div>
    <input type="text" placeholder="Nome" v-model="nome"/><br>
    <input type="text" placeholder="E-mail" v-model="email"/><br>
    <input type="text" placeholder="Telefone" v-model="telefone"/><br>
    <input type="text" placeholder="Endereço" v-model="endereco"/><br>
    <input type="text" placeholder="CPF" v-model="cpf"/><br>
    <button @click="cadastrar">CADASTRAR</button>
    <MeuComponente
      :nome="cadastro.nome"
      :email="cadastro.email"
      :telefone="cadastro.telefone"
      :endereco="cadastro.endereco"
      :cpf="cadastro.cpf"
    />
  </div>
</template>

<style scoped>
</style>  