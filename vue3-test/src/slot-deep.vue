<template>
  <MyBtn>
    <template #icon>
      <span>(B)</span>
    </template>
    <template #text>
      <span>Banana</span>
    </template>
  </MyBtn>
</template>

<script>
import MyBtn from '~/components/slot-deep-components' // 이를 props를 통해서 부모와 자식간에 데이터 통신

export default {
  components: {
    MyBtn
  }
}


</script>