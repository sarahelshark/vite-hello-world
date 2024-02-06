<script >
export default {
  name: 'App',
  data() {
    return {
      message: 'sarah',
      content: 'lorem ipsum dolor',
      msg:'lorem'
    }
  }
}
</script>

<template>
  <div class="wrapper">
    <h1>Hello {{ message }}</h1>
    <p>{{ content }}</p>
    <div>length:{{ msg.length }}</div>

    <input type="text" v-model="msg">
  </div>
</template>

<style ></style>
