<template>
  <div>
    <h1>I am app Layout</h1> 
    <AppHeader/>
    <nuxt />
  </div>
</template>

<script>
import AppHeader from '../components/AppHeader'

export default {
  components:{
     AppHeader,
     
  }
}

</script>

<style>
</style>
