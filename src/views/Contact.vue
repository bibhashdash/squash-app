<template>
  <h1>This is a contact page</h1>
  <div class="video-with-old-data">
    <div class="">
      {{ anyVariable }}
    </div>
    <form action="">
      <input type="text" v-model="name" placeholder="name" />
    </form>
    <div class="">
      <h2>Name is: {{ name }}</h2>
    </div>
    <button @click="clickHandler">Update Variable</button>
  </div>

  <div class="video-with-new-data">
    <div class="new-video">
      <video src="">
        {{ anyVariable }}
      </video>
    </div>
  </div>
</template>

<script>
import { ref } from "@vue/reactivity";
export default {
  setup() {
    const anyVariable = ref(0);
    const name = ref("");

    const clickHandler = () => {
      anyVariable.value++;
    };
    return { anyVariable, clickHandler, name };
  },
};
</script>

<style></style>
