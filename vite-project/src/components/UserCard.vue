
<script setup>
 const props = defineProps([
    'name','role','status'
 ])
 const emits = defineEmits(['view-profile'])
 const handleClick = () => {
    emits('view-profile', props.name)
 }
</script>

 <template>
    <div :class="['user-card', status]">
        <h3>{{ name }}</h3>
        <p>{{ role }}</p>
        <p v-if="status === 'Online'"> 🟢

        </p>
        <p v-else> 🔴</p>
        <button class = "btn"@click="handleClick">View Profile</button>
    </div>

    
 </template>


<style scoped>
.user-card{
    background-color: rgb(24, 3, 50);
    border: 2px solid #6b1250;
    border-radius: 20px;
    padding: 20px;
    width: 300px; 
    margin-left: 50px;
    text-align: center;
    color: white;
    box-shadow: 0 4px 8px rgba(0,0,0,0.2);
}

.user-card.Online{
    border-color: #4CAF50;
}
.user-card.Offline{
    border-color: #6b1250;
}
.btn{
     background-color: rgb(24, 3, 50);
     justify-content: center;
    border: 2px solid #6b1250;
    border-radius: 20px;
    padding: 20px;
    width: 150px; 
    font-size: 20px;
    text-align: center;
    color: white;
    box-shadow: 0 4px 8px rgba(0,0,0,0.2);
}
</style>
