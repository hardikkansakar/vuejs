<template>
  <!-- <h1 class="">Invoice Data</h1> -->
  <button @click="appnedDiv()" class="plus-btn">+</button>
  <button @click="getArrayData()" class="plus-btn">Get Data</button>
  <div class="main-div">
    <div class="sub-div">
      <table class="sub-div">
        <tr>
          <th>Product Name</th>
          <th>Category</th>
          <th>Price</th>
          <th>Discount</th>
          <th>Total</th>
          <th colspan="2"></th>
        </tr>
        <tr v-for="(invoice, index) in invoices" :key="index">
          <td>
            <input
              type="text"
              class="text-add"
              v-model="invoice.product_name"
            />
          </td>
          <td>
            <select type="dropdown" class="text-add" v-model="invoice.category">
              <option value="" disabled>Select City</option>
              <option value="ahmedabad">Ahmedabad</option>
              <option value="surat">Surat</option>
              <option value="baroda">Baroda</option>
              <option value="mehsana">Mehsana</option>
            </select>
          </td>
          <td>
            <input type="text" class="text-add" v-model="invoice.price" />
          </td>
          <td>
            <input type="text" class="text-add" v-model="invoice.discount" />
          </td>
          <td><input type="text" class="text-add" v-model="total" /></td>
          <td v-show="minusBtn">
            <button @click="removeDiv(index, invoice)" class="min-btn">
              -
            </button>
          </td>
        </tr>
      </table>
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
      invoices: [
        {
          product_name: "",
          category: "",
          price: "",
          discount: "",
          total: 0,
        },
      ],
      minusBtn: false,
      newArray: null,
      //   removeDiv: removeDiv--,
    };
  },
  methods: {
    appnedDiv() {
      this.minusBtn = true;
      this.invoices.push({
        product_name: "",
        category: "",
        price: "",
        discount: "",
        total: 0,
      });
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
  width: 504px;
  border: 1px solid;
  height: 86px;
  display: flex;
  margin-left: 330px;
  margin-top: 85px;
}
.sub-div {
  width: 100%;
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
</style>
