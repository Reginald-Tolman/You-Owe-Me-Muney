<template>
<!-- Can only have one div per templat  -->
  <div id="app">
    

    <NotificationPanel v-bind:currentUser="user" v-bind:control="controls"/>
    <Figure v-bind:currentUser="user" v-bind:control="controls" v-on:show-Modal="addCharge"/>

    <!-- <Figure debt="2000.00" unit= "$"/> -->

  </div>
</template>

<script>
// import Figure from "./components/Figure.vue";
import NotificationPanel from "./components/NotificationPanel";
import Figure from "./components/Figure";

export default {
  name: "app",
  components: {
    NotificationPanel,
    Figure
  },
  data() {
    return {
      controls:
      {
        AddChargeID: 0
      },
      user:
        {
          firstName: 'Daniel',
          lastName: 'Hall',
          debt: 2000,
          currency: '$',
          initials: 'D.H'
        }
    }
  },
  methods:
  {
    addCharge(id) {
      // Bring up Modal
      // Debt Displayed
      // Combobox for currency
      // Amount
      // Add, Cancel and X buttons
      console.log("Woah, Why am'I so generous all the time");
      this.user.debt += id;
    }
  }
};


</script>

<style>
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  body {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen-Sans, Ubuntu, Cantarell, "Helvetica Neue", sans-serif;
    line-height: 1.4;
  }
</style>
