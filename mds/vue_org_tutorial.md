> #### binding 으로 태그 속성제어하기
> [binding예제](https://vuejs.org/examples/#attribute-bindings)


```javascript
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

```
---
#### 한줄씩 뜯어보기
```javascript
    <span v-bind:title="message">
```
- `v-bind:title` 은 `:title` 로 줄여쓰기도 한다.
```javascript
    <span v-bind:title="message">
```
- `v-bind:title="message"` React를 생각하고 ""안에 `{message}` 라고 써야한다고 생각했는데 그냥 `"message"` 라고 쓴다.
```javascript
    <p v-bind:class="{ red: isRed }" v-on:click="toggleRed">
```
- `v-on:click="toggleRed"` 은 `@click="toggleRed"`로 쓸 수 있다.
요소에 대한 이벤트 처리는 보통 `@` 이 붙는다.
- `v-bind:class="{ red: isRed }"` 와 같이 red 라는 class를 포함할지 isRed 라는 data 값을 binding 을 통해 처리할 수 있다.
```javascript
toggleColor(){
  this.color = (this.color === 'green' ? 'green' : 'blue');   
}
```
- data 중 color의 값을 변경하는 로직을 단 한줄로 나타내었다. ( 혼자 풀었을 때는 if 분기문을 사용해서 4줄로 작성했는데 <span>3항 연산자</span>를 적극적으로 활용하자.)



