<template>
  <div id="default-template">
    <nuxt/>
  </div>
</template>

<script>
  import Vue from 'vue'
  import BootstrapVue from 'bootstrap-vue'
  Vue.use(BootstrapVue)
  //时间过滤器
  Vue.filter('formatDate',function (old) {
      function fillZero(value) {
          return value > 10 ? value : '0' + value;
      }
      let date = new Date(old)
      let year = fillZero(date.getFullYear());
      let month = fillZero(date.getMonth() + 1);
      let day = fillZero(date.getDate());
      let hours = fillZero(date.getHours());
      let second = fillZero(date.getSeconds());
      let minute = fillZero(date.getMinutes())
      return `${year}.${month}.${day} ${hours}:${minute}`
  })
  import 'bootstrap/dist/css/bootstrap.css'
  import 'bootstrap-vue/dist/bootstrap-vue.css'
  export default {

}
</script>

<style>

</style>
