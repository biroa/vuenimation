<template>
  <button type="button" @click="flag=!flag">Toggle 2</button>
  <transition name="zoom" type="transition" appear>
    <h2 v-if="flag">Hello</h2>
  </transition>
</template>
<script>
export default {
  name: 'CssAnimation',
  data(){
    return{
      flag:true
    }
  }
}
</script>
<style>
h2{
  width: 400px;
  padding: 20px;
  margin: 20px;
}

.zoom-enter-active {
  animation: zoom-in 1s linear forwards;
  transition: all 3s linear;
}

.zoom-leave-active {
  animation: zoom-out 1s linear forwards;
  transition: all 3s linear;
}
.zoom-enter-from{
  opacity: 0;
}
.zoom-enter-to{
  opacity: 1;
}

@keyframes zoom-in {
  from {
    transform: scale(0,0);
  }
  to{
  transform: scale(1,1);
  }
}

@keyframes zoom-out {
  from {
    transform: scale(1,1);
  }
  to{
    transform: scale(0,0);
  }
}

</style>
