<template>
  
</template>

<script>
export default {
  data(){
    return {
      names : ['손, 흥민', '황, 희찬', '김, 민재'],
      selectd : '',
      prefix : '',
      first : '',
      last : '',
    }
  },
  computed : {
    filteredNames(){
      return this.names.filter( (name) => name.startsWith(this.prefix))
    }
  },
  
}

</script>

