<template>
  <h1>{{ count }}</h1>
</template>

<script>
export default {
  data() {
    return {
      count: 2
    }
  },
  beforeCreate() { // 활용도 낮음
    console.log('333333', this.count); // 얘는 데이터가 정의되기전에 실행된다.이러면 count가 undefined
  },
  created() {
    console.log('222222!', this.count); // 순서에 상관 없음~~
  },
  beforeMount() {
    console.log('순서에 상관없다~~'); // 그래도 가독성을 위해서 순서 맞춰줘야함
    console.log(document.querySelector('h1')); // 여기서는 null 발생 why? 구조가 생성되기 전이기 때문에
  },
  mounted() {
    console.log('111111');
    console.log(document.querySelector('h1')); // 여기서는 잘나온다.
  },
  beforeCreate() { // 활용도 낮음
    console.log('4324343', this.count); // 얘는 데이터가 정의되기전에 실행된다.이러면 count가 undefined, 순서 상관없다~
  },
}
</script>
