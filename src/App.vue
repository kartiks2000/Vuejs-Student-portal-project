<template>
  <div>
    <Header @showadd="showit"></Header>
    <Addstudent v-if="addshow" @adding="addit"></Addstudent>
    <Students v-else :studentsinfo="studentsinfo" @deleteit="deleting"></Students>
    <Footer></Footer>
  </div>
</template>

<script>
import Header from './Components/header';
import Addstudent from './Components/addstudent';
import Students from './Components/students';
import Footer from './Components/footer';
export default {
  components:{
    Header : Header,
    Addstudent : Addstudent,
    Students : Students,
    Footer : Footer
  },
  data:function(){
    return{
      addshow : false,
      studentsinfo:[
        {name : "jfs",age : 15,course : "dcsd",session : "reger",id : "3r34rfgve"},
        {name : "wdfqwejfsefwe",age : 19,course : "awbgter",session : "regver",id : "34678968fbhftg"}
      ]
    }
  },
  methods:{
    addit(obj){
      this.studentsinfo.push(obj);
      this.addshow = !this.addshow;
    },
    deleting(myid){
      this.studentsinfo.map((i,idx) => {
        if(i.id == myid){
          this.studentsinfo.splice(idx,1);
        }
      });
    },
    showit(){
      this.addshow = !this.addshow;
    }
  }
}
</script>

<style scoped>

</style>