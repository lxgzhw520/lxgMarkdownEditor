<template>
  <div class="header">
    <div class="nav">
      <div class="logo">
        <img :src="imgSrc" alt="">
      </div>
      <div class="info">
        <button>注册</button>
        <button>登录</button>
      </div>
    </div>
  </div>
</template>

<script>
  import imgSrc from '../assets/logo.png'
  export default {
    name: "Vheader",
    data() {
      return {
        imgSrc:imgSrc,
      }
    }
  }
</script>

<style scoped>
  * {
    padding: 0;
    margin: 0;
  }

  .header {
    width: 100%;
    height: 40px;
    background-color: #fff;
    box-shadow: 0 2px 4px 0 #c9c9c9;
  }

  .header .nav {
    width: 980px;
    height: 40px;
    /*background-color: chartreuse;*/
    margin: 0 auto;
  }
  .nav .logo{
    width: 100px;
    height: 40px;
    float: left;
  }
  .logo img{
    height: 40px;
  }
  .nav .info{
    float: right;
    width: 200px;
    height: 40px;
  }
  .info button{
    width: 80px;
    height: 40px;
    float: left;
  }
</style>
