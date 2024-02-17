<script setup lang="ts">
import UsersList from './components/Users/UsersList.vue';

</script>

<template >
  <main class="Formato">
    <h1>Here we're going to share my users: </h1>
    <UsersList class="list" />
  </main>
</template>

<style scoped>  

.Formato{
  width: 100%;
  display: grid;

justify-content: center;
align-items: center;
}
h1 {
  text-align: center;
  width: 100%;
}
.list {
  
  padding: 12px;
}
#app{
  background-color: black ;
}
</style>
