<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
  </div>
  <div>{{ person.name }}</div>
  {{ person.cita }}
  <input type="text" v-model="person.cita" />
</template>

<script setup lang="ts">
import { reactive, onMounted } from "vue";

const person = reactive({
  name: "John Doe",
  cita: "",
});

onMounted(() => {
  changeName();
});

function changeName() {
  person.name = "Bakhrul";
}
</script>
