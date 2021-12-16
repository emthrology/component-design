<template>
  <check-box v-model="checked"></check-box>
</template>

<script>
import CheckBox from './components/CheckBox.vue';

export default {
  components: {
    CheckBox
  },
  data(){
    return {
      checked: true
    }
  }
}
//v-model이 돌아가는 구조를 통해 direct props mutations 방지
//동시에 상하위 컴포넌트 결합도 떡상
//datepicker, callendar, modal 등 세부적인 컴포넌트 작성시 유용한 테크닉
</script>
