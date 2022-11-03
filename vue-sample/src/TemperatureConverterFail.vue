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
      degree : 0,
    };
  },
  methods : {
    
  },
  computed : {
    getFahDeg(){
      return this.degree * (9/5) + 32;
    }
  }
}

</script>

