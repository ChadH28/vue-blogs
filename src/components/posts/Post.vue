<template>
  <div class="post">
      <h3>{{post.title}}</h3>
      <p>{{post.body}}</p>
      <span v-for="tag in post.tags" :key="tag">
          #{{tag}}
      </span>
      
  </div>
</template>

<script>
import { computed } from '@vue/runtime-core'
export default {
    props: [
        'post'
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