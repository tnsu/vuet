<template>
  <div class="about">
    <h1>This is an about page</h1>
    <tntis>
      <template v-slot:haeder="{tntis}">
        <p>haeder1 {{tntis }}</p>
      </template>
      <template #default>
      hello        
      </template>
    </tntis>
  </div>
</template>
<script>
import tntis from '@/components/subin.vue';

export default {
  components: {
    tntis
  }
}
</script>

<!--
// v-slot:haeder  #haeder  로 사용할 수 있음

      <template v-slot:haeder="props">
        <p>haeder1 {{ props.tntis }}</p> 를

       <template v-slot:haeder="{tntis}">
        <p>haeder1 {{tntis }}</p>  로 사용할 수 있음


 -->