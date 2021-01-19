<template>
  <div>
    <h1>This is Home page</h1>
    <tnti title="home title " name1="tnqsl"/>
  </div>
</template>

<script>
import tnti from '@/components/subin.vue';
export default {
  components:{
    tnti
  },

  data(){
    return{
      name: 'tnti'
    }
  }
}
</script>

<style scoped>
h1{
  color: rgba(79, 82, 255, 0.541);
}
</style>