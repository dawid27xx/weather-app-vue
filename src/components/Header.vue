<template>
    <header class="header">
        <h1>To do list</h1>
        <div id="nav">
            <router-link to="/">Home</router-link>
            <router-link to="/about">About</router-link>
        </div>
    </header>
</template>

<script>
export default {
    name: 'Header'
}
</script>

<style scoped>
    .header {
        background-color: #f2f2f2;
        padding: 20px;
        text-align: center;
    }
    #nav {
        margin-top: 20px;
    }
    #nav a {
        margin: 0 10px;
    }
</style>
