<template>
  <Registration />
  <Home msg="Welcome to my App" />
  
</template>

<script>
// import Home from './components/Home.vue';
import Registration from './components/RegForm.vue';
export default {
  name:'App',
  components:{
    Registration
  },
  methods: {
    handleClick() {
      this.active = !this.active;
    },
  },
    
  
}
</script>
