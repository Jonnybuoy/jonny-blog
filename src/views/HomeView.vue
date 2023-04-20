<template>
  <div class="home">
    <p>My name is {{ name }} and I am {{ age }} years old.</p>
    <button @click="handleClick">Click Me</button>
  </div>
</template>

<script>

export default {
  name: 'HomeView',
  setup() {

    let name = "Jonny"
    let age = 25

    const handleClick = () => {
      console.log("You clicked me")
    }

    return { name, age, handleClick }

  }
}
</script>
