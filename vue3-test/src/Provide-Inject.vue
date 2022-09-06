<template>
  <button @click="message = 'Good?'">
    Click!
  </button>
    <h1>App : {{ message }}</h1>
   <Patrnt />
</template>

<script>
import Parent from '~/components/Parent'
import { computed } from 'vue'


export default {
  components: {
    Parent
  },
  data() {
    return {
      message: 'Hello world!'
    }
  },
  provide() {
    return {
      msg: computed(() => {
        return this.message // 이런식으로 computed를 사용해서 작성해줄 수 있음
      })
    }
  }
}

</script>


<style scoped lang="scss">

</style>