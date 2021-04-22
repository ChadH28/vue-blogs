<template>
  <div class="home">
    <h1>Blogger</h1>
    <PostList :posts="posts"></PostList>

    <!--<h2>Refs</h2>
    <br />
    <h5>{{ user.name }}</h5>
    <h6>{{ user.age }}</h6>
    <button id="clicker" @click="handleAge">click me</button>
    <button @click="age++">increment age by 1</button>
    <button @click="age--">decrement age by 1</button>
    <div>
      <input type="text" v-model="user.name" />
      <input type="text" v-model="user.age" />
    </div> -->
    <!-- <h2>Computed</h2>
    <input type="text" v-model="search" />
    <p>Search term - {{ search }}</p>
    <div v-for="user in matchingUsers" :key="user">
      <h5>{{ user }}</h5>
    </div>
    <button @click="handleClick">stop watching</button> -->
  </div>
</template>
<script>
// @ is an alias to /src
import {
  ref,
  reactive,
  computed,
  watch,
  watchEffect,
} from "vue";
import PostList from "../components/posts/PostList";

export default {
  name: "Home",
  components: {
    PostList,
  },
  setup() {
    // const name = ref("chad");
    // const age = ref(22);

    // const user = ref({
    //   name: "Chadwick",
    //   age: 34,
    // });

    const posts = ref([]);
    const error = ref(null)

    return { posts };

    // const search = ref("");
    // const users = ref([
    //   "mario",
    //   "yosh",
    //   "amy",
    //   "ben",
    //   "sal",
    //   "kevin",
    //   "stewart",
    //   "clive",
    // ]);

    // const matchingUsers = computed(() => {
    //   return users.value.filter((user) => user.includes(search.value));
    // });

    // const stopWatch = watch(search, () => {
    //   console.log("w");
    // });

    // const stopEffect = watchEffect(() => {
    //   console.log("w", search.value);
    // });

    // const handleClick = () => {
    //   stopwatch();
    //   stopEffect();
    // };

    // const user2 = reactive({
    //   name: "Sally",
    //   age: 25,
    // });
    // const handleClick = () => {
    //   document.getElementById("clicker").innerHTML = "you clicked me";
    //   name.value = "Johann";
    //   age.value = 22;
    // };

    // const handleAge = () => {
    //   document.getElementById("clicker").innerHTML = "you updated the age";
    //   user.value.name;
    //   user.value.age;
    // };

    // const handleUser = () => {
    //   document.getElementById("clicker").innerHTML = "you updated the age";
    //   user2.name = "Stephanie";
    //   user2.age = 40;
    // };

    return {
      // name,
      // age,
      // handleClick,
      // user,
      // user2,
      // handleAge,
      // handleUser,
      // users,
      // search,
      // matchingUsers,
      // handleClick,
      posts,
    };
  },
  // created() {

  // },
  // mounted() {

  // }
};
</script> 
