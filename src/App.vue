<template>
  <h1
    :style="styleColor"
    @click="increase"
  >{{ count }}</h1>
  <div v-if="count > 5" class="box">
    <h3 style="color : orange; font-size: 30px;">div in box</h3>
  </div>
  <ul>
    <li
      v-for="fruit in fruits" :key="fruit"
    >{{ fruit }}</li>
  </ul>
  <button @click="increase">+1</button>
  <button @click="decrease">-1</button>
</template>

<script>
  export default {
    data() {
      return {
        count : 0,
        fruits : [
          'Apple', 'Banana', 'Cherry'
        ],
        styleColor :  {
          fontSize : '50px',
          color : 'royalblue',
          userSelect : 'none'
        }
      }
    }, 
    methods : {
      increase() {
        this.count += 1
      },
      decrease() {
        this.count -= 1
      }
    }
  }
</script>

<style>
#app {
  text-align: center;
  
}
</style>