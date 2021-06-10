<template>
<div class="app">
<!-- <p> {{name}} - {{age}}</p>
<button @click="changeName('Zelda')">Change name</button>
 <button @click="changeAge('30')">Change age</button> -->
<jobList :jobs="jobs"/>
</div>
</template>

<script lang="ts">
import Job from './types/Job'
import JobList from './components/JobList.vue'
// import { defineComponent, reactive,ref,toRefs } from 'vue';
import { defineComponent,ref } from 'vue';


export default defineComponent({
  name: 'App',
  components: {
    JobList
  },
  setup(){
    //with reactive values
    // const state = reactive({
    //   name: 'Link',
    //   age:25 as number | string
    // })
    // //need to return setup props as refs
    // return{ ...toRefs(state)}

    //with refs
    // const name = ref('Link');
    // const age = ref<number | string>(25);
    // return {name, age}
      const jobs = ref<Job[]>([
      { title: 'farm worker', location: 'lon lon ranch', salary: 30000, id: '1' },
      { title: 'quarryman', location: 'death mountain', salary: 40000, id: '2' },
      { title: 'flute player', location: 'the lost woods', salary: 35000, id: '3' },
      { title: 'fisherman', location: 'lake hylia', salary: 21000, id: '4' },
      { title: 'prison guard', location: 'gerudo valley', salary: 32000, id: '5' }
    ])
    return {jobs}
  },
  methods: {
    // changeName(name:string){
    //   this.name = name;
    //   console.log('name: ', name);
    //   return name;
    // },
    // changeAge(age: string|number){
    //   this.age=age;
    //      console.log('age: ', age);
    //   return age;
    // }
  }
});
</script>

<style>

</style>
