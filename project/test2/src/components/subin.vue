<template>
    <div>
        <p>header</p>
       <!-- <slot></slot> -->
        <p>body</p>
       <!-- <slot></slot> -->
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