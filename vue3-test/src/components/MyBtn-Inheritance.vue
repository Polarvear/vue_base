<template>
  <div class="btn">
    <slot></slot> <!--slot이랑 태그연결-->
  </div>
  <h1 v-bind="$attrs"></h1>
</template>


<script>


export default {
  inheritAttrs: false, //속성의 상속을 받지않겠다라는 뜻
  created() {
    console.log(this.$attrs); // 이렇게 특정 요소를 저장핤 ㅜ있음
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
  }

</style>