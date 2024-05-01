//npm run serve is how u start urvue app

<template>
  <div class="backdrop" @click.self = "closemodal">
    <div class="modal" :class="{dark:theme ==='dark'}">
      <h1>{{ header }}</h1>
      <p>{{ text }}</p>
    </div>
  </div>
</template>
<script>
export default{
  props:['header','text','theme'],
  methods:{
    closemodal(){
      this.$emit('close')
    }
  }
}
</script>

<style >
.modal{
  width: 400px;
  padding: 20px;
  margin: 100px auto;
  background-color: aliceblue;
  border-radius: 10px;
}
.backdrop{
  top: 0;
  position: fixed;
  background-color: hsl(0, 0%, 0% ,0.5);
  width: 100%;
  height: 100%;

}
.modal h1{
  color: rgb(60, 158, 125);
  border: none;
  padding: 0;
}
.modal p{
  font-style: normal;
}
.modal.dark{
 background-color: black;
 color: wheat;
}
.modal.dark h1{
  color: white;
}
  </style>