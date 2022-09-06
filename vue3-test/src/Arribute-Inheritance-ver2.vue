<template>
  <MyBtn @heropy="log" @chage-msg="logMsg">
    Banana
  </MyBtn>
</template>

<script>
import MyBtn from '~/components/MyBtn-Inheritance' // 이를 props를 통해서 부모와 자식간에 데이터 통신

export default {
  components: {
    MyBtn
  },
  methods: {
    log(e) {
      console.log('Click!');
      console.log(e);
    },
    logMsg(msg) {
      console.log(msg);
    }
  }
}


</script>