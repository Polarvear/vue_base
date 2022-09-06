<template>
  <div @click="increase">
    {{ count }}
  </div>
</template>


<script>
import { ref } from 'vue'
export default {

  setup() {
    let count = ref(0) // 이런식으로 반응성 가지게 할 수 있음
      function increase() {
        count.value += 1 // .value를 통해서 접근가능
      }

    return {
      count,
      increase
    }  
  }
}
</script>

<style scoped>

</style>