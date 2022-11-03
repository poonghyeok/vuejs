<template>
  <div>
    <h2>Text Input</h2>
    <input v-model="text">{{text}}
    <hr/>
    <h2>Check Box</h2>
    <input type="checkbox" v-model="checked" id="chkbox">
    <!-- binding까진 아니라 참조정도만 됨. checked 설정을 안하고 그냥 v-model만 했는데 체크 상태에 따라 데이터 바인딩이 가능해짐..! -->
    <label for="chkbox">Please Check</label>
    <hr />
    <h2>Multi CheckBoxes</h2>
    <input type="checkbox" v-model="checkedNames" id="checkJack" value="Jack">
    <label for="checkJack">Jack</label>
    <input type="checkbox" v-model="checkedNames" id="checkJohn" value="John">
    <label for="checkJohn">John</label>
    <input type="checkbox" v-model="checkedNames" id="checkMike" value="Mike">
    <label for="checkMike">Mike</label>
    <p>checkedNames : <pre>{{ checkedNames }}</pre></p>
    <!-- 그냥 checkbox 와 value로 배열 데이터로 바인딩도 가능... -->
    <hr/>
    <h2>Radio</h2>
    <input type="radio" v-model="picked" value="One">
    <input type="radio" v-model="picked" value="Two">
    <p>Selected : {{picked}}</p>
    <hr/>
    <h2>Select</h2>
    <select v-model="selected">
      <option value="A">A</option>
      <option value="B">B</option>
      <option value="C">C</option>
    </select>
    <span>Selected : {{selected}}</span>
    <!-- v-bind랑 v-model이랑 헷갈리지 마세요 -->
    <hr/>
    <h2>MultiSelect</h2>
    <select v-model="multiSelected" multiple>
      <option value="beenzino">빈지노</option>
      <option value="dok2">도끼</option>
      <option value="theQ">더콰</option>
    </select>
    <p>Selcted Rappers : {{multiSelected}}</p>
  </div>
</template>

<script>
export default {
  data(){
    return {
      text : 'Edit me',
      checked : true,
      checkedNames : [],
      picked : 'One',
      selected : 'A',
      multiSelected : []
    };
  }
}

</script>

