<template>
  <div class="container">
    
    <UserItem @goodbye="clikeado()" v-for="user in Users" :key="user.id" v-bind="user" />

    
  </div>

  <button class="BotonPadre" @click="clcikHandler">Click me</button>

</template>

<script setup lang="ts">
import UserItem from './UserItem.vue';
import Users from '@/data/UserData';


const clikeado = () => {
  alert('Goodbye');

}
const clcikHandler = (event:any) => {
  console.log(event);

}


</script>

<style scoped>
.container {
  display: grid;
  grid-template-columns: 1fr ;
  gap: 20px;
}

.BotonPadre{
  margin-top: 2%;
  width: 200px;
  background-color: green;
}

</style>