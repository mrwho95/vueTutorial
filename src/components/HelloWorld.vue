<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <!-- msg come from script props -->
    <alert mode="primary">First Alert</alert>
    <alert mode="danger">Second Alert</alert>
    <alert mode="success">Third Alert</alert>
    <alert mode="danger">Fouth Alert</alert>
    <div>
      <input type="text" v-model="lastname" placeholder="Your Name" />
      <!-- v-model connect data.lastname to the input -->
      <p>Welcome, {{lastname}}</p>
    </div>

    <button @click="ClickMe">Click Me</button>
    <!-- @click same as v-on:click -->
    <!-- <button v-on:click="ClickMe">Click Me</button> -->
    <!-- event handling Key Modifier refer to vue event handling documentation -->
    <input type="text" @keyup.enter="doSomething" placeholder="Please write your code" />

    <h3>Using Loop</h3>
    <ul>
      <!-- v-for == for loop -->
      <li v-for="person in students" :key="person">{{person}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  data() {
    return {
      lastname: "Ali",
      students: ["Ali", "Jan", "Dennis", "Henry"]
    };
  },
  methods: {
    ClickMe: function() {
      //old way create function
      console.log("You click on the button");
    },
    doSomething() {
      //new way create function
      console.log("Coupon Applied");
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
// li {
//   display: inline-block;
//   margin: 0 10px;
// }
a {
  color: #42b983;
}
</style>
