<template>
  <div>
    <h1 :class="{xxx:classed,add:!classed}">111</h1>
    <div @click="onclick">wode</div>
    <div @click="onclick2('111',$event)">123</div>
    <a 
      href="http://www.so.com"
      target="_blank"
      @click.passive="onclick3"></a>
      <el-button @click="onClick">点我</el-button>
      <input v-model="age"/>
      <h1>{{age}}</h1>
      <About :age="age" @xxx="onABc"/>
  </div>
</template>

<script>
// @ is an alias to /src
import About from './About'
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  data(){
    return{
      age:"小花"
    }
  },
  methods:{
    onClick(){
      this.age = new Date().getTime()
    },
    onABc(opt){
      console.log(opt,1)
    }
  },
  name: 'Home',
  components: {
    HelloWorld
  }
}
</script>
