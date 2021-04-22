<template>
  <div class="home">
    <h1>Blogger</h1>
    <p>
      This bloggers name is {{name}} and his age is {{age}}
    </p>
    <button id='clicker' @click="handleClick">click me</button>
  </div>
</template>

<script>
// @ is an alias to /src


export default {
  name: 'Home',
  setup() {
    let name = 'chad'
    let age = 22

    const handleClick = () =>{
      document.getElementById("clicker").innerHTML = 'you clicked me'
    }

    return {
      name,
      age,
      handleClick
    }
  },
  // created() {

  // },
  // mounted() {

  // }
}
</script>
