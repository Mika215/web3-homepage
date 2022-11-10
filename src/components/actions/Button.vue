<template>
  <button class="alami-btn">{{label}}</button>
</template>
<script>
  export default {
    name:"ActionButton",

    props : {

      label:{
        type:String,
        default:'Submit'
      }

    }
  }

</script>