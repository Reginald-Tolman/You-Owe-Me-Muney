<template>
<div class="Main">
  <div class="Figure">
    <h1>{{currentUser.currency}} {{currentUser.debt}}</h1>    
  </div>
  <div class="Buttons-Panel">
      <button class="Button" @click="$emit('show-Modal', 10)">Add</button>
      <button class="Button" @click="disputeCharge">Dispute</button>
      <button class="Button" @click="changeCurrency">Currency</button>
      <button class="Button" @click="viewHistory">History</button>
      
  </div>
</div>
</template>

<script>
export default {
  name: "Figure",
  props: 
    ["currentUser", "control"]
  ,
  methods: {


    disputeCharge() {
      console.log("False. All Charges are indisputable");
    },

    changeCurrency() {
      console.log("You can pay me in coffee.");
    },

    viewHistory() {
      console.log("View all transactions. Pretty dope right");
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.Main {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.Figure {
  display: flex;
  flex-direction: row;
  align-items: center;
  font-size: 3rem;
  position:relative;
  justify-content: center;
}

.Buttons-Panel
{
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
}

button
{
  padding: 5px; 
  text-align: center;
  margin-right: 5px ;

}

</style>
