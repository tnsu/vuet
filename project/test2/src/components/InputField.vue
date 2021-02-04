<template>
  <div>
     <label for="">Name</label>
     <input 
        type="text" 
        :value="name" 
        style="padding: 30px; border: 3px solid green;"
        @input="updateName"
        >
        <!-- 2. @input="$emit('update-name',$event)" 
        
       3.  <input 
        type="text" 
        :value="value" 
        style="padding: 30px; border: 3px solid green;"
        @input="$emit('input',$event.target.value)" 
        >

        -->
  </div>
</template>

<script>
export default {
  props:{
    name:{
      type: String,
      required : true
    }
    // 3.
    // value : {type: String, required : true}
  },
  methods: {
    updateName(e){
       console.log(e.target.value);
       this.$emit('update-name',e.target.value)
    }
  }
}
</script>