<template>
  <div>
    <input type="text" v-model="degree"> Celcius =
    <input type="text" v-model="getFahDeg"> Fahrenheit
  </div>
</template>

<script>
export default {
  data(){
    return {
      c: 0,
      f: 32,
    };
  },
  methods : {
    setC(e, )
  },
  computed : {
    getFahDeg(){
      return this.degree * (9/5) + 32;
    }
  }
}

</script>

