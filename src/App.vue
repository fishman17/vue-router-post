<template>
  <div id="app">
      <el-rate v-model="rate1" >

      </el-rate>
  </div>
</template>

<script>
import ElRate from '@/components/ElRate'

export default {
    data(){
        return{
            rate1: 3,
        }
    },
    components:{
        ElRate
    }
}
</script>

<style>

</style>
