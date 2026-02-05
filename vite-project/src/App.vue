<script setup>
import UserCard from './components/UserCard.vue'
</script>

<template>
  <div class = "container">
  <h1>Team Members</h1>
    <div class="member_list">
      <UserCard class = "member-card" name = "👧Melody" role = "Developer"/>
      <UserCard class = "member-card" name = "👦John" role = "Tester"/>
      <UserCard class = "member-card" name = "👧Alice" role = "Product Manager"/>
    </div>
</div>
>>>>>>> a1b8aa9 (Day 3 component task)
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

