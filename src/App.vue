<template>
  <button type="button" @click="flag=!flag">Toggle</button>
  <transition name="fade" mode="out-in">
    <h2 v-if="flag" key="main" >Animation One</h2>
    <h2 v-else key="secondary">Animation Two</h2>
  </transition>
  <css-animation/>
</template>

<script>
import CssAnimation from './components/CssAnimation';
export default {
  name: 'App',
  components: {
    CssAnimation
  },
  data(){
    return {
      flag:false
    }
  }
}
</script>

<style>
.fade-enter-from {
  opacity: 0;
}
.fade-enter-active{
  transition: all 3s linear;
}
.fade-leave-to{
  transition: all 3s linear;
  opacity: 0;
}
</style>
