<template>
  <div class="home">
    <h1>Refs</h1>
    <p >{{ ninjaOne.name }} - {{ninjaOne.age }}</p>
    <button @click="updateNinjaOne">Update Ninja One</button>
    <h1>Reactive</h1>
    <p >{{ ninjaTwo.name }} - {{ninjaTwo.age }}</p>
    <button @click="updateNinjaTwo">Update Ninja Two</button>
  </div>
</template>

<script>
import { ref, reactive } from 'vue'

export default {
  name: 'HomeView',
  setup() {

    const ninjaOne = ref({name: "Jonny", age: 25})
    const ninjaTwo = reactive({name: "Bash", age:21})

    const updateNinjaOne = () => {
      ninjaOne.value.age = 35
    }

    const updateNinjaTwo = () => {
      ninjaTwo.age = 25
    }

    return { ninjaOne, ninjaTwo, updateNinjaOne, updateNinjaTwo}

  }
}
</script>
