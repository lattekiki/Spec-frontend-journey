
<script setup>
 const props = defineProps([
    'name','role'
 ])
</script>

 <template>
    <div class = "user-card">
        <h3>{{ name }}</h3>
        <p>{{ role }}</p>
    </div>
 </template>


<style scoped>
.user-card{
    background-color: rgb(24, 3, 50);
    border: 2px solid #6b1250;
    border-radius: 20px;
    padding: 20px;
    width: 330px; 
    margin-left: 35px;
    text-align: center;
    color: white;
    box-shadow: 0 4px 8px rgba(0,0,0,0.2);
}
</style>
