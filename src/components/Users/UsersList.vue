<template>
  <div class="container">
    <UserItem v-for="user in Users" :key="user.id" v-bind="user" />
  </div>
</template>

<script setup lang="ts">
import UserItem from './UserItem.vue';
import Users from '@/data/UserData';


</script>

<style scoped>
.container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 20px;
}
</style>