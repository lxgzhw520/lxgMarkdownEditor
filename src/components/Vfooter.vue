<template>
  <footer>
    <ul>
      <li v-for="(item,index) in cityArray">{{item}}</li>
    </ul>
  </footer>
</template>

<script>
  export default {
    name: "Vfooter",
    data() {
      return {}
    },
    props: {
      //父子传值专用属性
      cityArray: Array,
    }

  }
</script>

<style scoped>

</style>
