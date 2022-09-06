<template>
  <div class="btn">
    <slot name="icon"></slot> <!--slot이랑 태그연결 컨텐트가 없는 경우 슬롯 사이에 있는 컨텐츠를 출력 가능 이걸 FallBack contents라고 부름-->
    <slot name="text"></slot> <!--이런식으로 순서 보장해줄 수 있음 v-slot의 축약어는 #-->
  </div>
</template>
<script>


export default {
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