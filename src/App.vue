<template>
  <h1>Hi Vue Cli</h1>

<!-- call stage -->

<div v-if="showModal">

<modal :theme="theme" @close="showModal=false"/>

<slot>
  <h1>Hi</h1>
  <p>Success</p>
</slot>

<slot>
  <h1>Hi</h1>
  <p>Delete?</p>
</slot>



</div>

  
  <button @click="showModal=true">open modal</button>
  <button @click="showDeleteModal=true">delete modal</button>

</template>

<script>
//import stage
import Modal from "./components/Modal.vue"

export default {

      data(){
        return{
            header:"Hi",
            content:"Welcome user Gi Gi",
            theme:"success",
            deletetheme:"delete",
            showModal:false,
            showDeleteModal:false
        }
      },
//Register stage
      components:{
        Modal
      }

    }
</script>

<style scoped>
h1{
  color: brown;
}
</style>