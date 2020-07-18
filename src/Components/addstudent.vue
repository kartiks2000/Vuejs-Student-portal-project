<template>
  <div>
      <h1>ADD STUDENT </h1>
    <div class="sec">
        <h1>Student name :</h1>
        <input type="text" v-model="studentinfo.name"/>
    </div>

    <div class="sec">
        <h1>Student age :</h1>
        <input type="number" v-model="studentinfo.age"/>
    </div>

    <div class="sec">
        <h1>Course :</h1>
        <input type="text" v-model="studentinfo.course"/>
    </div>

    <div class="sec">
        <h1>Session :</h1>
        <input type="text" v-model="studentinfo.session"/>
    </div>

    <div class="sec">
        <h1>Student ID :</h1>
        <input type="text" v-model="studentinfo.id"/>
    </div>

    <button @click="requestadding">ADD</button>

  </div>
</template>

<script>
export default {
  data:function(){
      return{
          studentinfo:{
              name : "",
              age : 0,
              course : "",
              session : "",
              id : ""  
          }
      }
  },
  methods:{
      requestadding(){
          this.$emit("adding",this.studentinfo);
      }
  }
}
</script>

<style scoped>
    div{
        text-align: center;
        color: rebeccapurple;
        padding: 2rem;
        background-color: gray;
    }
    .sec{
        width: 40%;
        background: cornsilk;
        margin: 2rem auto;
        padding: 1rem;
        display: flex;
        align-items: center;
        justify-content: space-around;
    }
    input{
        outline: none;
        border: 2px solid purple;
        border-radius: 50rem;
        padding-left: 2rem;
        width: 12rem;
        height: 2rem;
    }
    button{
        font-size: 1.5rem;
        margin: 1.6rem;
        padding: .5rem;
        color: purple;
    }
</style>