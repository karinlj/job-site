<template>
<div class="app">
<p> {{name}} - {{age}}</p>
<button @click="changeName('Zelda')">Change name</button>
 <button @click="changeAge('30')">Change age</button>
</div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'App',
  components: {
  },
  data(){
    return{
      name: 'Link',
      age:25 as number | string
    }
  },
  methods: {
    changeName(name:string){
      this.name = name;
      console.log('name: ', name);
      return name;
    },
    changeAge(age: string|number){
      this.age=age;
         console.log('age: ', age);
      return age;
    }
  }
});
</script>

<style>

</style>
