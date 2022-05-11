<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
  </div>
  <div>{{ person.name }}</div>
  {{ hobby }}
  <input type="text" v-model="hobby" />
</template>

<script setup lang="ts">
import { reactive, ref, onMounted } from "vue";

const hobby = ref("");
const person = reactive({
  name: "John Doe",
  cita: "",
});

onMounted(() => {
  changeName();
  hobby.value = "Mancing";
});

function changeName() {
  person.name = "Bakhrul";
}
</script>
