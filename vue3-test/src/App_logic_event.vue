<template>
  <div
   class="parent"
   @wheel.passive="handler"> <!--passive를 통해서 사용자에게 쾌적하게 사용하게 할 수 있음 화면과 로직의 분리-->
   <div
    class="child"></div> <!--e.stopPropagation === vue 의 stop-->
  </div>

</template>

<script>
export default {
  methods: {
    handler(e) {
      for (let i = 0; i < 10000; i++) {
        console.log(e);
      }
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
    overflow: auto;
    .child {
      width: 100px;
      height: 200px;
      background-color: orange;
    
    }
  }
</style>