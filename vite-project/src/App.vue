<script setup>
import UserCard from './components/UserCard.vue'
const showAlert = (userName) => {
  alert(`Viewing profile of:` + userName);
}
</script>

<template>
  <div class = "container">
  <h1>Team Members</h1>
    <div class="member_list">
      <UserCard class = "member-card" name = "👧Melody" role = "Developer" status = "Online" @view-profile="showAlert"/>
      <UserCard class = "member-card" name = "👦John" role = "Tester" status = "Online" @view-profile="showAlert"/>
      <UserCard class = "member-card" name = "👧Alice" role = "Product Manager" status = "Offline" @view-profile="showAlert"/>
    </div>
</div>
</template>
<style>
h1{
    margin-bottom: 40px;
    text-align: center;
    color: rgb(224, 237, 237);
    font-size: 40px;
}
.container{
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 20px;
    justify-content: center;
    min-height: 100vh;
}

.member_list{
  display: flex;
  flex-direction: row;
  gap: 20px;
  justify-content: center; 
}

.member-card{
  font-size: 20px;
}

</style>

