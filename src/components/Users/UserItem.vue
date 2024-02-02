<template>
  <div class="card">
    <h2>#{{ props.id }} {{ name }} | {{ props.lastName }}</h2>
    <h3>Email: <span>{{ props.email }}</span></h3>
    <h3>Age: <span>{{ props.age }}</span></h3>
    <h3>Email: <span>{{ props.email }}</span></h3>
    <input type="text" v-model="name">
  </div>
</template>

<script setup lang="ts">
import type { IuserInfo } from '@/interfaces/IUserInfo'
import { ref } from 'vue';

const props = defineProps<IuserInfo>()
const name = ref(props.name)

</script>

<style scoped>
.card {
  border: gray solid 1px;
  border-radius: 4px;
  padding: 8px 12px;
}
</style>