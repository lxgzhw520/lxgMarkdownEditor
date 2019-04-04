<template>
  <div class="wrap">
    <div class="t">
      <button @click="addCity">添加城市</button>
    </div>

    <div class="mark">
      <textarea name="" id="" cols="30" rows="10" class="editor" v-model="markValue">
      </textarea>
      <div class="show" v-html="currentValue">
      </div>
    </div>
  </div>
</template>

<script>
  import Marked from 'marked'

  export default {
    name: "Vcontent",
    data() {
      return {
        markValue: ''
      }
    },
    methods: {
      addCity() {
        //触发自定义的事件
        this.$emit('addCity', '回龙观')
      }
    },
    computed: {
      currentValue() {
        return Marked(this.markValue)
      }
    }
  }
</script>

<style scoped>
  .t {
    width: 300px;
    height: 100px;
  }

  .mark {
    width: 1210px;
    height: 600px;
    margin: 0 auto;
  }

  .editor, .show {
    float: left;
    width: 400px;
    height: 600px;
    border: 1px solid blue;
  }
</style>
