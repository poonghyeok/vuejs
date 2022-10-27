<template>
  <div>
    <button @click="toggleList">Toggle List</button>
    <button @click="pushNumber">Push Number</button>
    <button @click="popNumber">Pop Number</button>
    <button @click="reverseNumber">Reverse Number</button>
    <ul v-if="isListShow">
      <li v-for="(data, index) in dataList" :key="index">{{data}}</li>
      <span v-if="dataList.length === 0">data is empty</span>
    </ul>
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
