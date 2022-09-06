<template>
  <div
    v-bind="$attrs"
    class="btn"
    @click="hello">
    <slot></slot>
  </div>
</template>


<script>
import { onMounted } from 'vue'
export default {
  inheritAttrs: false,
  props: {
    color: {
      type: String,
      default: 'gray'
    }
  },
  emits: ['hello'],
  // mounted() {
  //   console.log(this.color);
  //   console.log(this.$attrs);
  // },
  // methods: {
  //   hello() {
  //     this.$emit('hello')
  //   }
  // },
  setup(props, context) { //this 를 가지고 올 수 없기 떄문에 매개변수로 넘겨줌
    function hello() {
      context.emit('hello') // $ 표시 없애야함
    }
     onMounted(() => {
      console.log(props.color);
      console.log(context.attrs);
    })

    return {
      hello
    }
  }
}
</script>

<style scoped>

</style>