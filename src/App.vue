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
      styles:' text-red bg-gray',
      count: 0 , //il mio conteggio parte da 0
      image:'https://picsum.photos/200/300'

    }
  },
  methods:{
    anotherFunction(){
      console.log('another function')
    },
    testFunction(){
      console.log('This is a method [a function inside an object]')
      console.log(this.message)
      this.anotherFunction();
    },
    greetUser(event){
      alert (`Ciao ${this.name}, nice to see you again!`)
      if (event){
        alert(event.target.name)
      }
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
        <input  type="text" v-model="name">
        <div></div>
        <label for="lastname"> Last name:</label>
        <input type="text" v-model="lastname">

        <p>
          Ciao {{  name }} {{ lastname }} , bentornato!
        </p> <!--tecnica mustache syntax-->

        <p v-bind:class="styles"> <!--class binding Forma estesa-->
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ducimus blanditiis, incidunt modi unde minus expedita rem, quas laudantium eum sint, in veritatis? Ea error incidunt amet quia, iure pariatur ab.
        </p>
        <p :class="styles"> <!--class binding Forma breve-->
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ducimus blanditiis, incidunt modi unde minus expedita rem, quas laudantium eum sint, in veritatis? Ea error incidunt amet quia, iure pariatur ab.
        </p>

        <button @click="testFunction">click</button>
        <button @click="greetUser">benvenuto</button>
        <button @click= "count++">click {{ count }}</button>  <!--NOTA BENE, ogni pezzo di codice contrnut tra "" di fatto si tratta di codice JS PLAIN -->
        <img :src="image" alt="random picture">
    </div>
  </div>
</template>

<style ></style>
