<template>
  <MyBtn 
  class="heropy"
  style="color: red;"
  title="Hello World!">
    Banana
  </MyBtn>
</template>

<script>
import MyBtn from '~/components/MyBtn-inheritance' // 이를 props를 통해서 부모와 자식간에 데이터 통신

export default {
  components: {
    MyBtn
  }
}


</script>