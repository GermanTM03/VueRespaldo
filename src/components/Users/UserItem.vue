<template>
  <div class="card">
    <h2>#{{ props.id }} {{ name }} | {{ props.lastName }}</h2>
    <h3>Email: <span>{{ props.email }}</span></h3>
    <h3>Age: <span>{{ props.age }}</span></h3>
    <h3>Email: <span>{{ props.email }}</span></h3>
    <!-- <input type="text" v-model="name"> -->
    <input type="text" v-model="change">
    <h1>{{ changev }}</h1>
    <button :disabled="validationchange" @click="clcikHandler()">Click me</button>
    

  </div>
</template>

<script setup lang="ts">
import type { IuserInfo } from '@/interfaces/IUserInfo'
import { ref,computed } from 'vue';
import type{ Ref } from 'vue';

const props = defineProps<IuserInfo>()
const name = ref(props.name)

const change:Ref<string> = ref('')


const  emitir =defineEmits(['Goodbye'])
const clcikHandler = () => {
    emitir('Goodbye')

}


const changev = computed(()=>change)
const validationchange = computed(()=> !(change.value.length > 1))
</script>


<style scoped>
.card {
  background-color: blueviolet;
  color: white;
  width: 300px;
  border: rgb(224, 0, 0) solid 2px;
  border-radius: 10px;

  padding: 8px 12px;
}
</style>