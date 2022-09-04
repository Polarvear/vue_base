<template>
  <a
   href="https://naver.com"
   target="_blank"
   @click.prevent.once="handler"> <!--preventDefault라는 메서드를 prevent라는 수식어로 간단하게 사용가능 once등 이벤트 체이닝 또한 가능-->
   Naver
  </a>
</template>

<script>
export default {
  methods: {
    handler(e) {
      //e.preventDefault(); //기본동작 방지 html의 기본동작 안시킬 때 사용
      console.log('ABC');
    }
  }
}

</script>


<style scoped>

</style>