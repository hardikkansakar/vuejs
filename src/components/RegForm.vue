<template>
  <div>
    <!-- <h1 class="reg-text">Registration Form</h1>
    <form>
        <table>
            <td>
                <label>First Name</label>    
                <input  type="text" name="first_name" value="">
            </td>
            <td>
                <label>Last Name</label>
                <input type="text" name="last_name" value="">
            </td>
            <td>
                <label>Gender</label>
                <input type="radio" name="gender" value="male">Male
                <input type="radio" name="gender" value="female">Female
            </td>
            <button class="sub-btn" @click="onSubmitReg"></button>
        </table>
    </form> -->

    <h1 class="reg-text">Get Selected Dropdown Value</h1>
    <h3>Select City</h3>
    <select>
      <option>Ahmedabad</option>
      <option>Surat</option>
      <option>Baroda</option>
      <option>Gandhinagar</option>
    </select>
    <h1 class="reg-text">Get Selected Checkbox Values</h1>
    <h3>Hobbies</h3>
    <label for="movie">Movie</label>
    <input type="checkbox" value="movie" v-model="hobbies" id="movie" />
    <label for="music">Music</label>
    <input type="checkbox" value="music" v-model="hobbies" id="music" />
    <label for="dancing">Dancing</label>
    <input type="checkbox" value="dancing" v-model="hobbies" id="dancing" />
    <h4>I like to : {{ hobbies }}</h4>

    <h1 class="reg-text">Get Selected Radio Value</h1>
    <h3>Gender</h3>
    <label for="male">Male</label>
    <input type="radio" value="male" v-model="gender" id="male" name="gender" />
    <label for="female">Female</label>
    <input
      type="radio"
      value="female"
      v-model="gender"
      id="female"
      name="gender"
    />
    <h4>I am a : {{ gender }}</h4>
    <h1 class="reg-text">Toggle Demo</h1>
    <h2 v-if="come">may i come?</h2>
    <h2 v-else="come">may i go!</h2>
    <button @click="come = !come">Click me!</button>
  </div>
</template>
<script>
export default {
  name: "RegForm",
  // props: {
  //   msg: string,
  // },
  data() {
    return {
      msg: "",
      first_name: "hardik",
      last_name: "Kansakar",
      hobbies: [],
      gender: null,
      come: true,
    };
  },
  methods: {
    onSubmitReg() {
      this.first_name = "Sahil";
      this.last_name = "Yadav";
    },
  },
};
</script>

<style scoped>
.reg-text {
  color: cornflowerblue;
  font-family: "Courier New", Courier, monospace;
}
h1 {
  color: black;
  font-size: large;
}
h3 {
  color: darkgreen;
  font-size: small;
}
h2 {
  color: blue;
}
</style>
