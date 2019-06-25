<template>
  <div>
    <div class="container">
      <div class="display">
      {{display}}
    </div>
    <span class=button-row v-bind:key="button.id" v-for="button in buttons">
      <button class=number-button v-on:click="displayNumber(button.name)">{{button.name}}</button>
    </span>
    </div>
  </div>
</template>

<script>
export default {
  name: "Buttons",
  props: ["buttons"],
  data: () => ({
    display: "",
    firstNumber: "",
    operator: "",
    lastNumber: "",
  }),
  methods: { 
    async displayNumber(buttonName) { 
      if (buttonName === "AC")
      this.display = "",
      this.firstNumber = "",
      this.lastNumber = "",
      this.operator = null

      else if (buttonName === "X")
      this.firstNumber = this.display,
      this.display = "",
      this.operator = buttonName

      else if (buttonName === "+")
      this.firstNumber = this.display,
      this.display = "",
      this.operator = buttonName

      else if (buttonName === "-")
      this.firstNumber = this.display,
      this.display = "",
      this.operator = buttonName

      else if (buttonName === "/")
      this.firstNumber = this.display,
      this.display = "",
      this.operator = buttonName

      else if (buttonName === "=")
      this.lastNumber = this.display,
      this.display = this.solve(parseInt(this.firstNumber), this.operator, parseInt(this.lastNumber))

      else 
      this.display = [...this.display, buttonName].join("")
    },

    solve(firstNumber, operator, lastNumber) {
      if (operator === "X")
      return firstNumber * lastNumber
      else if (operator === "/")
      return firstNumber / lastNumber
      else if (operator === "+")
      return firstNumber + lastNumber
      else if (operator === "-")
      return firstNumber - lastNumber
    }
  }
};

</script>

<style scoped>
  .number-button {
    background: blue;
    width: 50px;
    height: 50px;
    color: white;
    font-weight: bold;
    border-style: solid;
    border-width: 2px;
    border-radius: 50%;
    border-color: rgb(53, 13, 53);
  }
  .button-row {
    display: flex;
    padding: 2px;
 
    
  }
  .container {
    margin: auto;
    width: 240px;
    height: 10px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;

  }
  .display {
    background: black;
    color: white;
    width: 230px;
    margin-bottom: 5px;
    font-weight: bold;
    padding: 2px;
  }
</style>
