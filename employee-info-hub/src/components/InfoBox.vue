<template>
    <div class="flex-container">
        <h2>Employee Name </h2>
        <h2>Employee ID </h2>
        <h2>Email </h2>
        <img id="logo" src="https://img.icons8.com/?size=160&id=113856&format=png" alt="Company Logo"/>
    </div>
    <div v-for="employee of employeeDetails" :key="employee.id" >
       <SingleEmployee :employee=employee />
    </div>
</template>
<script>
import SingleEmployee from './SingleEmployee.vue'
export default {
    name: 'InfoBox',
    props:{
        employeeDetails: Array
    },
    components:{
        SingleEmployee
    } 
}
</script>
<style scoped>
    .flex-container{
        display:flex;
        justify-content:space-between;
        align-items:center;
        font-family: "Lora", serif;
        font-weight:500;
        margin:20px;
        padding:5px;
    }
    #logo{
        width:80px;
        height:80px;
    }
</style>