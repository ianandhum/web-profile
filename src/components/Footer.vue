<template>
    <footer>
      &copy; {{year}}
    </footer>
</template>


<style lang="scss" scoped>
    footer{
        width:100vw;
        display: flex;
        justify-content: center;
        padding:10px 0;
    }
</style>
<script>
export default {
    name:"footer-item",
    computed: {
        "year":function(){
        return new Date().getFullYear()
        }
  }
}
</script>
