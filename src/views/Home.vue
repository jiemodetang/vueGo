<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/>÷ -->
    <router-view/>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'÷
import instance from '../utils/http'
// 
import {PAGE_INIT} from '../utils/url';


export default {
  name: 'home',
  components: {
    // HelloWorld÷
  },
  mounted(){
    console.log(PAGE_INIT)
    // // 为给定 ID 的 user 创建请求
    // instance.post(PAGE_INIT,qs.stringify({a:1}))
    //   .then(function (response) {
    //     console.log(response);
    //   })
    //   .catch(function (error) {
    //     console.log(error);
    //   });
    // }
     instance.get('/api/shakespeare/v2/notes/8493282fe232/book')
      .then(function (response) {
        console.log(response);
      })
      .catch(function (error) {
        console.log(error);
      });
    }
}
</script>
