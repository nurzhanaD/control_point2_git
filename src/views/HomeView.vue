<script setup>
    import cardComponent from '../components/cardComp.vue';
</script>
<template>
<div class="homeView">
    <nav class="navbar navbar-expand-lg navbar-light bg-light" style="width:100vw">
        <div class="container-fluid">
            <router-link class="navbar-brand" to="/" style="font-size:2rem;">Home</router-link>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarColor03" aria-controls="navbarColor03" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>

            <div class="collapse navbar-collapse" id="navbarColor03">
                <ul class="navbar-nav me-auto">
                    <li class="nav-item">
                        <router-link class="nav-link" to="/register" style="font-size:1.5rem;">Register</router-link>
                    </li>
                    <li class="nav-item">
                        <router-link class="nav-link" to="/login" style="font-size:1.5rem;">Login</router-link>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
    <br>
    <cardComponent title="Cat"/>
    <cardComponent title="Dog"/>
    <cardComponent title="Bird"/>
</div>
</template>
<style scoped>
.homeView{
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: lightblue;
}
</style>
