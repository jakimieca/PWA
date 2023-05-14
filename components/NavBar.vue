<template>
<div class="navbar">
    <div>
        <NuxtLink to="/home" class="navbar-link">Home</NuxtLink>
        <NuxtLink to="/gallery" class="navbar-link">Galeria</NuxtLink>
    </div>
</div>

</template>

<script>
export default{
name: 'NavBar'
}


</script>

<style scoped>
.navbar{
    background-color: #f9c2ec;
    padding: 20px;
}

.navbar-link{
    text-decoration: none;
    color: black;
    padding: 15px;
}

.navbar-link:hover{
background-color: #e1afd5;
padding: 10px;
}


</style>

