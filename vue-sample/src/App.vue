<template>
  <div>
    <div v-on:mouseover="showTooltip" v-on:mouseleave="showTooltip" >잠시 마우스를 올려두면 타이틀이 보입니다.</div>
    <span v-if="tooltip">제가 타이틀입니다.</span>
    <div v-bind:class="toggle ? 'basic' : 'toggle'" v-on:click="toggleOn">저는 원래 검정색입니다. 한번 클릭하면 빨간 색으로 바뀝니다.</div>
    <div v-bind:class="dymColor == 'green' ? 'green' : 'blue'" v-on:click="changeColor">저는 초록색입니다. 한번 클릭하면 파란색으로 바뀝니다.</div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data(){
    return {
      toggle : false,
      dymColor : 'green',
      tooltip : false,
    };
  }
  ,
  methods : {
    showTooltip(){
      setTimeout(() => {
        this.tooltip = !this.tooltip;
      }, 500)
      
    },
    toggleOn(){
      this.toggle = !this.toggle;
    }
    ,
    changeColor(){
      if(this.dymColor == 'green'){
        this.dymColor = 'blue';
      }else{
        this.dymColor = 'green';
      }
    }
  },
}

// https://vuejs.org/examples/#attribute-bindings
</script>

<style>
.toggle{
  color : red;
}

.green{
  color : green;
}

.blue{
  color : blue;
}
</style>
