<script>
export default {
  name: 'Greeting',
  data() {
    return {
      msg: 'Hello World'
    }
  },
  props: ["age"]
}
</script>

<template>
  <div>
    <p v-if="age>25">{{ msg }}</p>
    <p v-else>you must be 25 years or older to view this page</p>
  </div>
</template>

<style lang="scss" scoped>

</style>