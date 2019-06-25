<template>
  <div>
    <Buttons v-bind:buttons="buttons"/>
  </div>
</template>

<script>
import Buttons from './Buttons.vue';

export default {
  name: "Calculator",
  components: {
    Buttons
  },
  data() {
    return{
      buttons: [
        {
          id: 1,
          name: "AC",

        },
         {
          id: 2,
          name: "+/-",
        },
         {
          id: 3,
          name: "%",
        },
         {
          id: 4,
          name: "/",
        },
         {
          id: 5,
          name: "7",
        },
         {
          id: 6,
          name: "8",
        },
         {
          id: 7,
          name: "9",
        },
         {
          id: 8,
          name: "X",
        },
         {
          id: 9,
          name: "4",
        },
         {
          id: 10,
          name: "5",
        },
         {
          id: 11,
          name: "6",
        },
         {
          id: 12,
          name: "-",
        },
         {
          id: 13,
          name: "1",
        },
         {
          id: 14,
          name: "2",
        },
         {
          id: 15,
          name: "3",
        },
         {
          id: 16,
          name: "+",
        },
         {
          id: 17,
          name: "0",
        },
         {
          id: 18,
          name: "NA",
        },
         {
          id: 19,
          name: ".",
        },
         {
          id: 20,
          name: "=",
        },
      ]
    }
  }
};
</script>

<style scoped>
</style>
