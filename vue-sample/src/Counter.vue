<template>
  <div>
    <button v-on:click="countUp">up</button>
    <button v-on:click="countDown">down</button>
    <button v-on:click="countReset">reset</button>
    <p>{{count}}</p>
  </div>
</template>

<script>
export default {
  data(){
    return {
      count : 0,
    };
  },
  methods : {
    countUp(){
      this.count = this.count+1;
    },
    countDown(){
      this.count = this.count-1;
    },
    countReset(){
      this.count = 0;
    }
  }
}

</script>

