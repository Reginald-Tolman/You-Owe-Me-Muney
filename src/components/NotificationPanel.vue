<template>
  <div class="NotificationPanel">
    <div class="Start"><h3>Debt Tracker</h3></div>
    <div class="Center"><h3>You Owe Me Money</h3></div>
    <div class="End">      
      <div class="Initials"><h3 class="Name">{{currentUser.initials}}   </h3></div>
      <div class="Notification-Icon"><i class="far fa-bell"></i>
        <div class="Notification-Count">3</div>
      </div>    
      <div class="Transaction-Icon"><i class="far fa-money-bill-alt"></i></div>    
    </div>
  </div>
</template>

<script>
export default {
  name: "NotificationPanel",
  props: ["currentUser"]
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.NotificationPanel 
{
  display: flex;
  flex-direction: row;
  height: 56px;
  padding: 0 16px;
  color: white;  
  justify-content: space-between;
  align-items: center;
  background-color: #262626;
}

.Start
{
  display: flex;
  align-items: center;

}

.Center
{
  display: flex;
  align-items: center;

}

.End
{
  display: flex;
  align-items: center;
}

.Initials
{
  display: flex;
  line-height: 18px;  
  padding-right: .8rem;
}

.Initials h3
{
  font-size: 1rem;
}

.Notification-Icon i
{
  display: flex;
  vertical-align: middle;
  display: inline;
  padding-right: .8rem;
  line-height: 18px;
  font-size: 2rem;
}

.Transaction-Icon i
{
  display: flex;
  vertical-align: middle;
  display: inline;
  padding-right: .8rem;
  line-height: 20px;
  font-size: 2rem;

}

.Notification-Count
{
  position: absolute;
  top: 4px;
  color: white;
  background-color: #c00;
  width: 18px;
  height: 18px;
  border-radius: 50%;
  line-height: 18px;
  font-size: 10px;
  text-align: center;
  cursor: pointer;
}
</style>
