<template>
  <Hello ref="hello"/>
</template>

<script>
import Hello from '~/components/Hello'
export default {
  components: {
    Hello
  },
  //created() // 여기서는 참조할 수 없음 
  mounted() {
    console.log(this.$refs.hello.$refs.good); //refs의 개념 컴포넌트가 html에 연결된 직후에만 사용가능함 $el이라는 속성을 써줘야지 참조가능함 refs속성 줬을때는 $refs사용
  }
}

</script>


<style scoped lang="scss">


</style>