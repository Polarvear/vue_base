<template>
   <MyBtn>Banana</MyBtn>
   <MyBtn :color="color"
            text="Banana"/> <!--숫자 데이터를 넣기 위해서는 v-bind를 통해서 연결해줘야함 :color=123이런식으로-->
   <MyBtn large color="red"
          text="Banana">Banan</MyBtn> <!--이런식으로 slot을 통해 출력가능 slot은 span 태그도 가능-->
   <MyBtn 
          text="Banana"/>
    <button>Banana</button>
</template>

<script>
import MyBtn from '~/components/MyBtn' // 이를 props를 통해서 부모와 자식간에 데이터 통신
export default {
  components: {
    MyBtn
  },
  data() {
    return {
      color: '#000'
    }
  }
}


</script>


<style scoped lang="scss">

</style>