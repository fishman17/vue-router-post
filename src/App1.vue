<template>
  <div id="app">
    <el-badge class="item" :value="1" :max="9">
    <el-button nativeType="submit" size="medium" @click="addComment()">评论</el-button>
    </el-badge>
    <el-badge class="item" :value="4" :max="9" isDot>
    <el-button size="small" type="primary" >回复</el-button>
    </el-badge>
    <el-badge class="item" :value="32" :max="9">
    <el-button size="mini" type="primary" icon="el-icon-edit">点我</el-button>
    </el-badge>
    <el-button :disabled="saveDisabled" @click="doSave()"  size="medium" type="text">发布</el-button>
  </div>
</template>

<script>
import ElBadge from '@/components/ElBadge'
import ElButton from '@/components/ElButton'

export default {
  data(){
    return{
      saveDisabled: true
    }
  },
  name: 'app',
  components: {
    ElButton,
    ElBadge
  },
  mounted(){
    setTimeout(()=>{
      this.saveDisabled = false;
    },5000)
  },
  methods:{
    addComment(){
      console.log('1zz');
    },
    doSave(){
      console.log('fabu');
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
