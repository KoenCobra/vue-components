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
}
</script>

<template>
  <h3>Hey</h3>
  <Greeting :age="age"/>
  <User :age="age" @age-change="age++"/>
</template>


