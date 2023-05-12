<template>
  <div>
    <!-- <Registration /> -->
    <!-- <Home msg="Welcome to my App" /> -->
    <!-- <p></p> -->
    <!-- <button @click="empFilteredData()">Click Me</button> -->
  </div>
  <div>
    <div v-if="seeMe">
      <p>i am a first text seen by if</p>
    </div>
    <div v-else>
      <p>i am a default else text</p>
    </div>

    <button @click="clickIfMe()">Click Me I am if</button>
  </div>
  <div>
    <div v-show="showMeHere">
      <p>i am a show text</p>
    </div>
    <button @click="clickToShowMe()">Click Me i am Show</button>
  </div>
  <div>
    <div v-for="(elm,index) in 10" :key="index">
      <p>{{ index }} - {{ elm }}</p>
    </div>
    
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      // empList:[],
      emp: [
        { empName: "Juhi", empID: 12, empSalary: 1000 },
        { empName: "Mahi", empID: 13, empSalary: 5000 },
        { empName: "Test", empID: 14, empSalary: 1500 },
        { empName: "Vaishali", empID: 15, empSalary: 2000 },
      ],
      seeMe: false,
      showMeHere: false,
    };
  },
  methods: {
    empFilteredData() {
      const newEmpList = this.emp.filter((elem) => {
        return elem.empSalary > 1500;
      });

      console.log("newEmpList", newEmpList);
    },
    clickIfMe() {
      this.seeMe = true;
    },
    clickToShowMe() {
      this.showMeHere = true;
    },
  },
};
</script>
