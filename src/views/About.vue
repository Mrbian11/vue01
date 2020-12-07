<template>
  <div class="about">
    <h1 @click="onclick">This is an about page</h1>
  </div>
</template>
<script>
  export default {
    props:['age'],
    methods:{
      onclick(){
        this.$emit('xxx',{
          username:"边晨旭"
        })
      }
    }
  }
</script>
