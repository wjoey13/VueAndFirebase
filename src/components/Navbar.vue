<template>
    <nav class="main-navbar">
        <ul>
            <li><router-link :to ="{name: 'Home'}">Home</router-link></li>
            <li><router-link :to ="{name: 'About'}">About</router-link></li>
        </ul>
        <h2>User Profiles</h2>
        <ul>
            <li v-for="(id, index) in userIds" :key="index">
                <router-link :to="{name:'ViewProfile', params:{ user_id: id }}">
                 <span>Profile {{ id }}</span>
                </router-link>
            </li>
        </ul>
        <h2>Navagation controls</h2>
        <ul>
            <li><button @click="goHome">Redirect to Home</button></li>
        </ul>
    </nav>
</template>
<script>
export default {
    name: 'Navbar',
    data(){
        return {
            userIds:['1','2','3','4']
        }
    },
    methods:{
        goHome(){
            this.$router.push({name: 'Home'})
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
