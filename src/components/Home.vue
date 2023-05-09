<template>
    <div>
        <h1>Home Component</h1>
        <h2>This is {{ userName }}</h2>
        <h2>{{ msg }}</h2>
        <button @click="onClickMe">Click me</button>
    </div>
</template>
<script>


export default {
    name:'Home',
    props:{
        msg:String,
    },
    data(){
        return{
            userName:'Hardik'    
        }
        
    },
    methods: {
    onClickMe() {
      this.userName = 'Sahil';
    },
  },
}
</script>
<style>
.btn {
  border: 1px solid gray;
  padding: 8px 16px;
  border-radius: 5px;
  font-family: 'Segoe UI';
  font-weight: bold;
}
.active {
  background-color: white;
  color: black;
}

.non-active {
  background-color: blue;
  color: white;
}
</style>
