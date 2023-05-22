<template>
  <!-- <h1 class="">Invoice Data</h1> -->
  <button @click="appnedDiv()" class="plus-btn">Add Room</button>
  <!-- <button @click="getArrayData()" class="plus-btn">Get Data</button> -->
  <div class="main-div" v-for="(elm, index) in ageCount" :key="index">
    <div class="sub-div">
      <h2>Room {{ ++index }}</h2>
      <div class="content-div">
        <div>
          <h4>Adult</h4>
          <button @click="incrementAge(elm)">+</button>
          <input type="text" v-model="elm.adultAge" />
          <button @click="decrementAge(elm)">-</button>
        </div>
        <div class="child-div">
          <h4>Child</h4>
          <button @click="childIncrementAge(elm)">+</button>
          <input type="text" v-model="elm.childAge" />
          <button @click="childDecrementAge(elm)">-</button>
        </div>
      </div>
    </div>
  </div>
  <div>
    <p>{{ newArray }}</p>
  </div>
</template>
<script>
export default {
  name: "DemoInvoice",
  data() {
    return {
      ageCount: [
        {
          adultAge: 1,
          childAge: 1,
        },
      ],
    };
  },
  methods: {
    appnedDiv() {
      this.ageCount.push({
        adultAge: 1,
        childAge: 1,
      });
    },
    incrementAge(elm) {
      elm.adultAge++;
    },
    decrementAge(elm) {
      if (elm.adultAge != 0) {
        elm.adultAge--;
      }
    },
    childIncrementAge(elm) {
      elm.childAge++;
    },
    childDecrementAge(elm) {
      if (elm.childAge != 0) {
        elm.childAge--;
      }
    },
    removeDiv(index, invoice) {
      var row = this.invoices.indexOf(invoice);
      if (row > 0) {
        this.invoices.splice(row, 1);
      }
    },
    getArrayData() {
      const arrayData = this.invoices.map((elem, index, arr) => {
        return (this.newArray = arr);
      });
    },
  },
};
</script>

<style scoped>
.main-div {
  width: 254px;
  border: 1px solid;
  height: 125px;
  display: flex;
  margin-left: 330px;
  margin-top: 85px;
}
.sub-div {
  width: 100%;
  padding-left: 20px;
  padding-right: 20px;
}

.content-div {
  display: flex;
}
.child-div {
  margin-left: 40px;
}
.text-add {
  width: 100%;
}
.plus-btn {
  background-color: aqua;
  font-size: 15px;
  height: 36px;
  width: 120px;
}
.min-btn {
  background-color: rgb(219, 36, 60);
  font-size: 15px;
  width: 25px;
}
table,
th,
td {
  border: 1px solid black;
}
input {
  width: 30px;
  margin: 5px;
}
</style>
