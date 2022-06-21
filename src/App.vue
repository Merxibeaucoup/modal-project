<template>
  <h1> {{title}}</h1>
  <P>welcome.....</P>

  
  <div v-if="showModal">
      <Modal  theme="sale" @close="Modal" >
      <h1>GREAT DAY TO GET JIGGY</h1>
      <p>yeeeeee buddy!..........</p>
     <template v-slot:links>
      <a href="#">Sign Up</a>
      
      <a href="#"> more Info</a>
     </template>
      </Modal>

  </div>

  <div v-if="showModalTwo">
      <Modal  theme="" @close="ModalTwo" >
      <h1>GREAT DAY TO GET JIGGY</h1>
      <p>yeeeeee buddy!..........</p>
     <template v-slot:links>
      <a href="#">Sign Up</a>
      
      <a href="#"> more Info</a>
     </template>
      </Modal>

  </div>

  <button @click="Modal"> open modal</button>
  <br>

  <button  @click="ModalTwo"> second Modal </button>
</template>

<script>

import Modal from './components/Modal.vue'


export default {
  name: 'App',
  components:{Modal},
 data(){
  return{
  title: ' my first Vue App :)',
  showModal: false,
  showModalTwo: false

 }
}, 
methods:{
  Modal(){
    this.showModal = !this.showModal;
  }, 
  ModalTwo(){
    this.showModalTwo = !this.showModalTwo;
  }
}

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h1{
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}
</style>
