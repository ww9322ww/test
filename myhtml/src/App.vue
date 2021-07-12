<template>
  <div id="page-box">
    <img src="http://127.0.0.1:9000/upload/a.jpg" alt="" />
    <h1>123456456</h1>
  </div>
</template>

<script>
import axios from 'axios';
export default{
  data(){
      return{
        text:''         /* 定义一个函数 text 格式是字符串*/ 
      }
  },
  mounted(){       /*定义一个生命周期*/
  this.getData()
},
  methods:{
    getData(){
      axios({
        method:'get',
        url: 'http://127.0.0.1:9000/api/'
       
      }).then((res)=>{
        console.log(res)
      }
      
      )
  
    }
  },
}
</script>

<style>
#page-box {
  width: 300px;
  height: 600px;
  box-shadow: 0 2px 12px 0 black;
  margin: 0 auto;
}
</style>
