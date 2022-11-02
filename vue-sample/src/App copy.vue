<template>
  <div>
    <h3>Text Input</h3>
    <h3>Checkbox</h3>
    <h3>Multi Checkbox</h3>
    <h3>Radio</h3>
    <h3>Select</h3>
    <h3>Multi Select</h3>
  </div>
</template>

<script>
export default {
  name: 'app',
  data(){
    return {
      isListShow : false,
      dataList : [],
      num : 0,
    };
  }
  ,
  methods : {
    toggleList(){
      this.isListShow = !this.isListShow;
    },
    pushNumber(){
      this.dataList.push(this.num++);
    },
    popNumber(){
      this.dataList.pop();
      this.num--;
    },
    reverseNumber(){
      this.dataList.reverse();
    },
  }
}


// https://vuejs.org/examples/#attribute-bindings
</script>

<style>
  .red{
    color : red;
  }
</style>
