<template>
  <button @click="add">
    ADD
  </button>
  <h1>{{ reversedMsg }}</h1> <!--처음에 캐싱한번 함-->
  <h1>{{ reversedMsg }}</h1>
  <h1>{{ reversedMsg }}</h1>
  <h1>{{ reversedMsg }}</h1>
</template>



<script>
export default {
  data() {
    return {
      //Setter, Getter
      msg: 'Hello Computed!'
    }
  },
  computed: { // 얘는 사용할 때 뒤에 () 해줄 필요 없음 why? 계산된 하나의 데이터이기 때문 
              // 캐싱이라는 기능이 있음 그래서 한번 연산해놓은 데이터가 있으면 다시한번 연산하지 않음
              // 주로 데이터를 최적화 하는 기능이 있을 때 사용함
              // readonly 기능임 즉 getter
    // reversedMsg() {
    //   return this.msg.split('').reverse().join('')
    // }

    //reversedMsg를 Getter / Setter로 만드는 방법
    reversedMsg : { // 자주 사용하지는 않지만 Vuex에서 가끔 사용하는 패턴임
      get() {
        return this.msg.split('').reverse().join('')
      },
      set(newValue) {
        this.msg = newValue
        console.log(newValue); // 이렇게 값 확인 가능
      }
    }
  },
  methods: {
    add() {
      this.reversedMsg += '!?'
      // this.msg += '!?'
    }
  }
}
</script>
