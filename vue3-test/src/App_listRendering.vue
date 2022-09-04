<template>
<button @click="handler">
  Click me!
</button>
  <ul>
    <li
      v-for="{ id, name } in newFruits" 
      :key="id"> <!--하나의 li태그가 고유하다는 것을 v-bind를 통해서 명시해줌/ 두번째 매개변수를 통해 순서를 보여줄 수도 있음 key는 고유하게 존재해야함**-->
      {{ name }}-{{ id }}
    </li>
  </ul>
</template>



<script>
import shortid from 'shortid'
export default {
  data() {
    return {
      fruits: ['Apple', 'Banana', 'Cherry'] // 배열에서 고유하게 존재하는 id = index 같은 게 필요함
    }
  },
  computed: {
    newFruits() {
      return this.fruits.map(fruit => ({
        // 객체 데이터 반환 즉 map을 통해 가공된 데이터 반환됨
          id: shortid.generate(), // 이렇게 하면 고유한 값을 가지게 만들 수 있음 
          name: fruit
      }))
    }
  },
  methods: {
    handler() {
      this.fruits.push('pushed Orange!') // 데이터를 바꾸면 화면이 바뀐다 반응성~~!!
    }
  }
}

</script>


<style scoped>

</style>