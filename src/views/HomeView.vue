<template>
  <div class="home">
    <p ref="p">My name is {{ name }} and I am {{ age }} years old.</p>
    <button @click="handleClick">Click Me</button>
    <button @click="age++">Add age by 1</button>
    <input type="text" v-model="name">
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  name: 'HomeView',
  setup() {

    // const p = ref(null)

    const name = ref("Jonny")
    const age = ref(25)

    const handleClick = () => {
      name.value = "Gibbz"
      age.value = 25
      
    }

    return { name, age, handleClick }

  }
}
</script>
