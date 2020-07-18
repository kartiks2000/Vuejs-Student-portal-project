<template>
  <div>
    <Student @click.native="deleterequesting(st.id)" v-for="st in studentsinfo" :key="st.id">
        <h2>NAME : {{st.name}}</h2>
        <h2>AGE : {{st.age}}</h2>
        <h2>COURSE : {{st.course}}</h2>
        <h2>SESSION : {{st.session}}</h2>
        <h2>ID : {{st.id}}</h2>
    </Student>
  </div>
</template>

<script>
import Student from './student';
export default {
  components:{
      Student : Student
  },  
  props:["studentsinfo"],
  methods:{
      deleterequesting(myid){
          this.$emit("deleteit",myid);
      }
  }
}
</script>

<style scoped>
    div{
        height: 70vh;
        overflow: scroll;
    }
    
</style>