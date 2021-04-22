<template>
  <div class="post">
      <h3>{{post.title}}</h3>
      <p>{{post.body}}</p>
  </div>
</template>

<script>
export default {
    props: [
        'posts'
    ],
    setup(props) {
        const snippet = computed( () => {
            return props.post.body.substring(0,100) + '.....'
        }) 
    }
}
</script>

<style>

</style>