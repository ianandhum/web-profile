<template>
  <div id="app">
    <router-view/>
    <Footer/>
  </div>
</template>
<style lang="scss">

  @import 'scss/variables';

  #app{
    display:flex;
    flex-direction: column;
    flex-grow: 1;
    min-height: 100%;
    header{
      width:100vw;
      height:$header_height;
    }
    main{
      flex-grow: 1;
      
    }

    &> footer{
      color:rgb(100, 120, 122);
    }
  }
  body{
    margin:0;
    height:100vh;
    width:100vw;
    font-family: $fonts;
    overflow-x:hidden;
    font-size:$font_size;
    color:$color;
    background-color:$bgcolor;
  }
</style>
<script>
import Footer from "@/components/Footer"
export default {
  name:"app",
  components:{
    Footer
  }
}
</script>


