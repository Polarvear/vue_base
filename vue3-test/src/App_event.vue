<template>
  <h1 v-bind:[attr]="'active'"  <= 이렇게하면 하나의 문자데이터로 적용할 수 있음 class이름에 느낌표 계속 붙는 상황 수정
    @[event]='add'>
    {{msg}}
  </h1>
</template>

<script>

export default {
  data() {
    return {
      msg: 'active',
      attr: 'class',
      event: 'click' //@click 말고 이렇게도 줄 수 있음
    }
  },
  methods: { // methods로 써줘야함
    add() {
      this.msg += "!"
    }
  }
}

</script>

<style scoped>
  .active {
    color: aqua;
  }
</style>