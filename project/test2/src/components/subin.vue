<template>
    <div>
        <p>header</p>
       <slot name="haeder" :tntis="tntis"></slot>
        <p>body</p>
       <slot name="body"></slot>
        <p>footer</p>
    </div>
</template>

<script>
export default {
    props:{
        title:{
            type:String,
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
            tntis : "수빈"
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