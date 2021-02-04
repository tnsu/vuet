<template>
  <div>
    <h1>This is Home page</h1>
 <form action="">
   <InputField :name="name" @update-name="updateName"/>
  <!--
    1.주석처리 된것은 메서드를 주석처리후 해제하면 사용가능하다 
     <InputField :name="name" @update-name="name = $event.target.value"/>  -->
  <!--
    2.   <InputField v-model="name" />
    -->


   <br><button>Submit</button>
 </form>
 {{name}}
  </div>
</template>

<script>
import InputField from '@/components/InputField.vue'
export default {
  components:{
    InputField
  },
  data(){
    return{
      name: ''
    }
  },
  methods:{
    updateName(name){
      this.name = name;
    }
  }
}
</script>

<style scoped>
h1{
  color: rgba(79, 82, 255, 0.541);
}
</style>