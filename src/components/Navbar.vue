<template>
    <nav class="main-navbar">
        <ul>
            <li><router-link :to ="{name: 'Home'}">Home</router-link></li>
            <li><router-link :to ="{name: 'About'}">About</router-link></li>
        </ul>
    </nav>
</template>
<script>
export default {
    name: 'Navbar',
    data(){
        return {
            
        }
    }
}
</script>
<style>
ul{
    list-style-type: none;
    padding: 0;
}
a{
    color: 42b983;
}
</style>
