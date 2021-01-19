<template>
    <div>
        <h1>{{ title }} </h1>
        <p>{{ name1 }}</p>
        <p>{{ name }}</p>
        <button @click="updateName">changeName</button>
    </div>
</template>

<script>
export default {
  //  props: ['title'],
    props:{
        title:{
            type:String,
         //   requierd: true,
            default:'defaut title'
        },
        name1:{
             type:String,
            default:'defaut name'
        }
    },
    data(){
        return{
            name : 'tntis',
        }
    },

    methods:{
        updateName(){
            this.name= "tntis Updated";
        }
    }
}
</script>

<style scoped>

</style>