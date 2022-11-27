<template>
    <nav class="navbar">
        <router-link to="/" class="navbar-link">Home</router-link>
        <router-link to="/game" class="navbar-link">Game</router-link>
        <router-link to="/resources" class="navbar-link">Ressources</router-link>
    </nav>
</template>

<script>
export default {
    name: "NavBar"
};
</script>

<style scoped>
.navbar {
    background-color: #fff;
    border: 1px solid #ccc;
    border-radius: 4px;
    color: #333;
    cursor: pointer;
    display: inline-block;
    font-size: 14px;
    font-weight: 400;
    line-height: 1.42857;
    margin-bottom: 0;
    padding: 6px 12px;
    text-align: center;
    vertical-align: middle;
    white-space: nowrap;
}

.navbar-link {
    background-color: #fff;
    border: 1px solid #ccc;
    border-radius: 4px;
    color: #333;
    cursor: pointer;
    display: inline-block;
    font-size: 14px;
    font-weight: 400;
    line-height: 1.42857;
    margin-bottom: 0;
    padding: 6px 12px;
    text-align: center;
    vertical-align: middle;
    white-space: nowrap;
    margin-right: 10px;
}

.navbar-link:hover {
    background-color: #eee;
}

.navbar-link:active {
    background-color: #ddd;
}

.navbar-link:disabled {
    background-color: #ccc;
    color: #999;
    cursor: not-allowed;
}
</style>