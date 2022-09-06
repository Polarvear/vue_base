<template>
  <div class="btn">
    <slot></slot> <!--slot이랑 태그연결-->
  </div>
    <h1 @dblclick="$emit('heropy', 123)"> <!--두번째 인수로 데이터 넘겨줄 수 있음 -->
    ABC
  </h1>
  <input type="text" 
         v-model="msg" />
</template>


<script>


export default {
  emits: [ // 이런식으로 배열로 연결 가능
    'heropy',
    'chageMsg'
  ],
  data() {
    return {
      msg: ''
    }
  },
  watch: {
    msg() {
      this.$emit('chageMsg', this.msg);
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
  }

</style>