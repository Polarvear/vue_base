<template>
  <Fruits />   <!--div태그들을 Fruits라는 태그로 변경 가능-->
</template>

<script>

import Fruits from '~/components/Fruits'
export default {
  components: { // 옵션을 객체 데이터로 선언
    Fruits
     //Fruits 라는 컴포넌트를 연결 가능
  }
}
</script>
