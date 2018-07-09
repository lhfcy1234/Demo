<template>
    <div class="b">
      <el-row>
        <el-col :span="12" class="aaa" ref="c"> wwwww</el-col>
      </el-row>
      <div ref="d"></div>
    </div>
</template>

<script>
    export default {
        name: "Layout",
        mounted (){
         let aHeight = document.body.clientHeight;
          console.log(aHeight)
          console.log( this.$refs.c)
          //this.$refs.c.style.height = aHeight+'px';
          this.$refs.d.style.height = aHeight+'px';
          //普通的元素上有style 组件上面没这个属性所以
          //this.$refs.c.style.height = aHeight+'px'; 报错
          //this.$refs.c.style为undefined
        }
    }
</script>

<style scoped>
  .b{
    height: 500px;
  }
  .aaa{
    background:red;
    border-right:1px solid blue;
  }
</style>
