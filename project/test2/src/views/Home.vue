<template>
  <div>
    <h1>This is Home page</h1>
 <!-- <form action=""> -->
  <!--1)
   <InputField :name="name" @update-name="updateName"/>
  -->
  <!--
    1.주석처리 된것은 메서드를 주석처리후 해제하면 사용가능하다 
     <InputField :name="name" @update-name="name = $event.target.value"/>  -->
  <!--
    2.   
    <InputField v-model="name" />
    -->
    <InputField :name="name"/>


   <!-- <br><button>Submit</button> -->
       <br><button @click="updateName">Submit</button>
 <!-- </form> -->
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
      name: 'tnti'
    }
  },
  
  //1
  // methods:{
  //   updateName(name){
  //     this.name = name;
  //   }
  // },

  // 인스턴스 라이프 사이클
  beforeCreate(){
    console.log('beforeCreate :', this.name)  // data에 접근이 불가능 
  },

  created(){
    // 가장 많이 사용하기도함
    console.log('created : ', this.name) // data에 접근 가능해짐 서버에 요청을 보낼때 많이 사용 
  },

  beforeMount(){
    //alert('beforeMount')
    // DOM 이 mount가 되지 않아서  id=app 에 내용이 없음 (body 에 내용이 없음 
   console.log('beforeMount : ', this.name)
  },
  mounted(){
    //alert('mounted')
    // app 안에 내용이 채워지면서 화면에 접근이 가능 , dom을 control 하고싶으면 여기서 하면 됨
   console.log('mounted : ', this.name)
  },
  beforeUpdate(){
    //alert('beforeUpdate')
    // data가 바뀌기전에 
   console.log('beforeUpdate : ', this.name)
  },
  updated(){
    //alert('updated')
     console.log('updated : ', this.name)
  },
  beforeUnmount(){
    //alert('beforeUnmount')
    // 다른 페이지를 클릭시 지금의 컴포넌트가 없어지면서 실행
     console.log('beforeUnmount : ', this.name)
  },
  unmounted(){
    //alert('unmounted')
    // 메모리 누수를 방지하기위해 이벤트리스너 삭제, 데이터 초기화때 사용하기도 한다
     console.log('unmounted : ', this.name)
  },
  methods: {
    updateName(){
      this.name= 'TNTI';
    }
  }
}
</script>

<style scoped>
h1{
  color: rgba(79, 82, 255, 0.541);
}
</style>

<!-- 

  The  `beforeDestroy` lifecycle hook is deprecated. Use `beforeUnmount` instead  vue/no-deprecated-destroyed-lifecycle
   The `destroyed` lifecycle hook is deprecated. Use `unmounted` instead



-->