<template>
  <div>
    <h3>{{message}}</h3>
    <button v-on:click="reverseMsg">Reverse Message</button>
    <button v-on:click="appendChar">Append !</button>
  </div>
</template>

<script>
export default {
  name: 'app',
  data(){
    return {
      message: 'hello vuejs!',
    };
  }
  ,
  methods : {
    reverseMsg(){
      this.message = this.message.split("").reverse().join("");
    },
    appendChar(){
      this.message = (this.message + '!');
    }
  },
}
</script>

<style>
