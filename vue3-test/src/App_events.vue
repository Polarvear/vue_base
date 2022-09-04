<template>
  <div
   class="parent"
   @click="handlerA"> <!--캡쳐링을 통해 parent를 먼저 동작 시킴 capture 수식어 self <= 그 영역을 정확하게 클릭을 했을 때 그 영역만 동작하게 함-->
   <div
    class="child"
    @click="handlerB"></div> <!--e.stopPropagation === vue 의 stop-->
  </div>

</template>

<script>
export default {
  methods: {
    handlerA(e) {
      console.log(e.target);
      console.log(e.currentTarget);
      console.log('A');

    },
    handlerB(e) {
      //e.stopPropagation(); // 이벤트 버블링
      console.log('B');
    }
  }
}

</script>


<style scoped lang="scss">
  .parent {
    width: 200px;
    height: 100px;
    background-color: royalblue;
    margin: 10px;
    padding: 10px;
    .child {
      width: 100px;
      height: 100px;
      background-color: orange;
    
    }
  }
</style>