<template>
  <input type="checkbox" :value="value" @click="toggleCheckBox">
</template>

<script>
export default {
  //v-model 돌아가는 구조는 아래와 같다 
  // @input 이벤트를 통해 emit 하고
  // :value 값 으로 값 bind 함

  props: {
    value: {
      type:Boolean,
    }
  },
  methods :{
    toggleCheckBox(){
      this.$emit('input', !this.value)
    }
  }
  
}
</script>