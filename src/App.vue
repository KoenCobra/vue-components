<script>
import Greeting from "@/components/Greeting.vue";
import User from "@/components/User.vue";

export default {
  name: 'App',
  components: {User, Greeting},
  data(){
    return{
      age: 20
    }
  },
  methods:{
    updateChange(ageNumber){
      this.age += ageNumber;
    },
    updateAgeCallBack(ageNumber){
      this.age += ageNumber;
    }
  }
}
</script>

<template>
  <h3>Hey</h3>
  <Greeting :age="age"/>
  <User :ageChangeFunction="updateAgeCallBack" :age="age" @age-change="updateChange"/>
</template>


