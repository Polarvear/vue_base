<template>
  <section v-if="hasFruits">
    <h1>Fruits</h1>
    <ul>
      <li 
        v-for="fruit in fruits" 
        :key="fruit">
        {{ fruit }}
      </li> <!--데이터 바인드의 약어로 : <= 기호 사용-->
    </ul>
  </section>
  <section>
    <h1>ReverseFruits</h1>
    <ul>
      <li
       v-for="fruit in reverseFruits" 
       :key="fruit">
       {{ fruit }}
       </li>
    </ul>
  </section>
</template>

<script>
export default {
  data() {
    return {
      fruits : [
        'Apple', 'Banana', 'Cherry'
      ]
    }
  },
  computed: {
    hasFruits() {
      return this.fruits.length > 0
    },
    reverseFruits() {
      return this.fruits.map(fruit => {
        return fruit.split('').reverse().join('')
      })
    }
  }
}
</script>
