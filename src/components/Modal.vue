<template>
  <div class="backdrop" @click="closeModal">
      <div class="modal" :class="{success:theme=='success', danger:theme=='delete'}">
          <p>{{header}}</p>
          <p>{{content}}</p>
      </div>

  </div>
</template>

<script>
export default {
    props:['header','content','theme'],

    methods:{
        closeModal(){
            this.$emit("close")
        }
    }
}
</script>

<style scoped>

    .backdrop{
        position: fixed;
        top: 0%;
        background-color: rgba(192, 207, 192, 0.6);
        width: 100%;
        height: 100%;
    }

    .modal{
        width: 400px;
        padding: 20px;
        margin: 100px auto;
        background-color:greenyellow;
        border-radius: 10px;
    }
      .success{
        background-color: green;
        color: white;
    }

    .danger{
        background-color:crimson;
        color: white;
    }

</style>