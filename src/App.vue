<template>
<h1> {{ title }}</h1>
<p>welcome...</p>
<div  v-if="showmodal">
   <Model :header="header" :text="text" theme="dark" @close="toggleModal"/>
</div>
    <button @click.alt ="togglemodal">open modal</button> <br><br>
</template>
<script>
import Modal  from './components/Modal.vue';
export default {
  name:app,
  components:{Modal},
  data(){
  return {
    title:' first vue app',
    header:'signup for give away',
    text:'subscribe now',
    showmodal: false
  }
},
  methods: {
    togglemodal(){
  this.showmodal = !this.showmodal;
 } 
},

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
</style>
