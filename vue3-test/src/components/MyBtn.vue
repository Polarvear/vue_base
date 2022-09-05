<template>
  <div 
  :class="{ large }"
  :style="{ backgroundColor: color }"
  class="btn">
    <slot></slot> <!--슬롯 부분에 우리가 만든 태그안에 내용을 출력해줄 수 있음 <MyBtn>내용</MyBtn>-->
  </div>
</template>

<script>

export default {
  props: { //속성을 정해주는 옵션임
    color: {
      type: String,
      defalut: 'gray' 
    },
    large: {
      type: Boolean,
      defalut: false
    }
  }
}

</script>


<style scoped lang="scss">
  .btn{
    display: inline-block;
    margin: 4px;
    padding: 6px 12px;
    border-radius: 4px;
    background-color: gray;
    color: white;
    cursor: pointer;
    &.large {
    font-size: 20px;
    padding: 10px 20px;
    }
  }

</style>