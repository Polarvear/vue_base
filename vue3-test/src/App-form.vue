<template>
   <h1>{{ msg }}</h1>
  <input
    type="text"
    v-model="msg"/> <!--양방향 바인딩 간소화-->
    <h1>{{ checked }}</h1>
    <input type="checkbox"
    v-model="checked" />
</template>
<!--
  :value="msg"
    @input="msg = $event.target.value" /> 이 부분을 통해 양방향 데이터 바인딩 e라고 써주면 안됨 event라고 써줘야함 
-->

<script>
export default {
  data() {
    return {
      msg: 'HelloWorld!', // 단방향 데이터 바인딩 methods 를 추가하여 데이터 양방향 바인딩
      checked: false
    }
  }
  //methods: {
    //handler(e) {
      //console.log(e.target.value); 
      //this.msg = e.target.value; // 이 상태가 양방향 데이터 바인딩 이 문장을 6번의 $뒤에 써줌 
    //}
  //}
}

</script>


<style scoped lang="scss">

</style>