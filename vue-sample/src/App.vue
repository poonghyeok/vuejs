<template>
  <div>
    <p>
      <span v-bind:title="message">
        여기다가 마우스를 올려놓으면 잠시 뒤에 툴팁을 볼 수 있습니다.
      </span>
    </p>

    <p v-bind:class="{ red: isRed }" v-on:click="toggleRed">
    저는 원래 검점색입니다. 클릭을 하게 되면 빨간 색으로 변하게 되죠. 
    </p>

    <p v-bind:style="{ color : color }" v-on:click="toggleColor">
      저는 녹색과 파란색을 왔다 갔다 합니다. 클릭해보세요. 
    </p>
  </div>
</template>

<script>
export default {
  name: 'app',
  data(){
    return {
      message : "hello vuejs!",
      color : 'green',
      isRed : false,
    };
  }
  ,
  methods : {
    toggleRed(){
      this.isRed = !this.isRed;
    },
    toggleColor(){
      this.color = (this.color === 'green' ? 'green' : 'blue');   
    }
  }
}


// https://vuejs.org/examples/#attribute-bindings
</script>

<style>
  .red{
    color : red;
  }
</style>
