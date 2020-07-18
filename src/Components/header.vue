<template>
  <div>
    <h1>STUDENT PORTAL</h1>
    <button @click="addinitiation">ADD NEW STUDENT</button>
  </div>
</template>

<script>
export default {
  methods:{
      addinitiation(){
          this.$emit("showadd");
      }
  }
}
</script>

<style scoped>
    div{
        padding: 2rem;
        background-color: skyblue;
        text-align: center;
    }
    button{
        font-size: 1.5rem;
    }
</style>