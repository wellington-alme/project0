<template>
  <div v-if="nome || email || telefone || endereco || cpf">
    <h3>Informações Cadastradas:</h3>
    <p><strong>Nome:</strong> {{ nome }}</p>
    <p><strong>E-mail:</strong> {{ email }}</p>
    <p><strong>Telefone:</strong> {{ telefone }}</p>
    <p><strong>Endereço:</strong> {{ endereco }}</p>
    <p><strong>CPF:</strong> {{ cpf }}</p>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  nome: string
  email: string
  telefone: string
  endereco: string
  cpf: string
}>()
</script>