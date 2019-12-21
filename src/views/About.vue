<template>
  <div class="about">
    <h1>This is an about page</h1>
    <h2>{{c}}</h2>
  </div>
</template>

<script>
import  {bar} from "./export";

export default {
  data(){
    return{
      aboutTest:''
    }
  },
  computed:{
    c(){
      return this.$store.state.a
    }
  },
  mounted(){
    // this.aboutTest = this._.join([1,2],'-')
    this.aboutTest = bar
  }
}
</script>
