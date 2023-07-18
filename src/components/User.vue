<script>
export default {
  name: "User",
  props: {
    age: {
      type: Number,
      // required: true,
      // default: 20
      validator(value) {
        return value < 130
      }
    },
    ageChangeFunction: Function
  },
  emits: ['age-change'],
  methods: {
    onClickAge() {
      this.$emit('age-change', 3)
    },
  },
  computed: {
    ageDoubled() {
      return this.age * 2;
    },
    isAgeValid() {
      return this.age < 130;
    }
  }
}
</script>

<template>
  <button :disabled="!isAgeValid" @click="onClickAge">Increment age event</button>
  <button :disabled="!isAgeValid" @click="ageChangeFunction(3)">Update age Callback</button>
  <p>the user is {{ age }} years old</p>
  <p>{{ ageDoubled }}</p>
</template>

<style scoped lang="scss">

</style>