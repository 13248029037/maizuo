<template lang="html">
  <div class="">
    <p>test</p>
  </div>
</template>

<script>
export default {
  created(){
var obj={a:9};
Object.defineProperty(obj,"a",{
  set(newVal){
    console.info("set");
    this["a"]=newVal;
  },
  get(){
    console.info("get")
    console.info(this);
return this["a"];
  }
})
window.obj=obj;
}
}
</script>

<style lang="css" scoped>
</style>
