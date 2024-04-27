<template>
    <Header/>

<main>
  <router-view/>

</main>
</template>
<script>
 import Header from './components/Header.vue';
export default {
  components:{
    Header
  },
  setup(){

    return{

    }
  }
}
</script>
<style lang="scss">
*{
  margin:0;
  padding: 0;
  box-sizing: border-box;
  font-family: sans-serif;

&::selection{
  background: transparentize(#42B883,0.5);
}
}
body{
  background-color: #35495E;
}
a {
  text-decoration: none;
}

</style>
