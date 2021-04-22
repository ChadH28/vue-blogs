<template>
  <div>
    <div class="post-list"></div>
    <div v-for="post in posts" :key="post.id">
      <Post :post="post"></Post>
    </div>
    <button @click="showPosts = !showPosts">toggle button</button>
  </div>
</template>

<script>
import { onMounted, onUpdated, onUnmounted } from "@vue/runtime-core";
import Post from "./Post";
export default {
  props: ["posts"],
  components: {
    Post,
  },
  setup(props) {
    onMounted(() => console.log("component mounted "));
  },
};
</script>

<style>
</style>