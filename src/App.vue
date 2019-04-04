<template>
  <div id="app">
    <Vheader></Vheader>
    <!--  自定义事件  -->
    <Vcontent @addCity="addCity"></Vcontent>
    <!--  绑定自定义属性  -->
    <Vfooter :cityArray='citys'></Vfooter>
    <img :src="imgSrc" alt="">
    <h2>{{currentMsg}}</h2>
    <ul>
      <li v-for="(item,index) in beauty">
        <a href="javascript:;">{{item}}</a></li>
    </ul>
    <button @click="clickHandler">点击</button>
  </div>
</template>
<script>
  //静态资源 图片 也可以导入为模块
  import imgSrc from './assets/logo.png'
  import Vheader from "./components/Vheader";
  import Vcontent from "./components/Vcontent";
  import Vfooter from "./components/Vfooter";

  export default {
    name: 'app',
    data() {
      return {
        msg: 'hhh',
        imgSrc: imgSrc,
        beauty: [
          '刘亦菲',
          '范冰冰',
          '楚冰冰',
        ],
        citys: [
          '北京',
          '天津',
          '上海',
          '重庆',
          '贵阳',
        ]
      }
    },
    methods: {
      clickHandler() {
        this.msg = '学Vue'
        this.beauty.push('baby')
      },
      addCity(city) {
        // alert('aaa')
        alert(city)
        this.citys.push(city)
      }
    },
    computed: {
      currentMsg() {
        return this.msg
      },
      getArray() {
        return this.beauty
      }
    },
    components: {
      Vheader, Vcontent, Vfooter
    }
  }
</script>
<style>

</style>
