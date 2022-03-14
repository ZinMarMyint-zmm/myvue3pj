<template>
  <h1>Hi</h1>
  <div v-if="showModal">
    <BackModal theme="success" @close="showModal=false">
     <h1>Login sucess</h1>
     <p>welcome user zin mar myint</p>
     </BackModal>
  </div>
  <button @click="showModal=true">Log in</button><br>

  <div v-if="deleteModal">
    <BackModal theme="delete" @close="deleteModal=false">
      <h1>Delete success</h1>
      <p>Your modal is deleted</p>
     </BackModal>
  </div>
  <button @click="deleteModal=true">Delete</button>
</template>

<script>
import BackModal from "./components/BackModal.vue"
export default {
  data(){
   return{
     
     
     showModal:false,
     deleteModal:false
   }
  },
  components:{
    BackModal
  }
  
}
</script>

<style scoped>
h1{
color:blue;
}
</style>
