<script>
export default {
  name: "User",
  props: ["age"],
  emits: ['age-change'],
  methods: {
    onClickAge() {
      this.$emit('age-change', 3)
    }
  },
  computed: {
    ageDoubled() {
      return this.age * 2;
    }
  }
}
</script>

<template>
  <button @click="onClickAge">Increment age</button>
  <p>the user is {{ age }} years old</p>
  <p>{{ageDoubled}}</p>
</template>

<style scoped lang="scss">

</style>