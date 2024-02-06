<script >
export default {
  name: 'App',
  data() {
    return {
      message: 'sarah',
      content: 'lorem ipsum dolor',
      msg:'lorem',
      name:'',
      lastname:'',

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
    <div></div>
    <div>
        <label for="name"> First name:</label>
        <input type="text" v-model="name">
        <div></div>
        <label for="lastname"> Last name:</label>
        <input type="text" v-model="lastname">
        <div></div>
        <p>
          Ciao{{ ' '+ name + ' ' +lastname}}, bentornato!
        </p> <!--tecnica mustache syntax-->
        
    </div>
  </div>
</template>

<style ></style>
