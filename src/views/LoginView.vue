<template>
    <div class="loginView">
        <h1>Log in to your account</h1>
        <form class="card" @submit.prevent="submitHandler">
        <div class="form-group">
            <label for="InputEmail1" class="form-label mt-4">Email address</label>
            <input type="email" class="form-control" id="InputEmail1" aria-describedby="emailHelp" placeholder="Enter email">
            <small id="emailHelp" class="form-text text-muted">We'll never share your email with anyone else.</small>
        </div>
        <div class="form-group">
            <label for="InputPassword1" class="form-label mt-4">Password</label>
            <input type="password" class="form-control" id="InputPassword1" placeholder="Password">
        </div>
        <div class="form-group">
            <label for="Select1" class="form-label mt-4">User status</label>
            <select class="form-select" id="Select1">
                <option>user</option>
                <option>admin</option>
            </select>
        </div>
        <br>
        <button type="submit" class="btn btn-outline-secondary">Log in</button>
    </form>
        <router-link to="/" style="font-size:1.4rem;">Go to Home.</router-link>
        <span style="font-size:1.4rem;">Don't have an account? <router-link to="/register">Register here.</router-link></span>
    </div>
</template>
<style scoped>
.loginView{
    margin:0;
    padding:0;
    height:100vh;
    display:flex;
    justify-content: center;
    align-items: center;
    background-color: pink;
    text-align: center;
    flex-direction: column;
}
form{
    width:50vw;
}
.btn-outline-secondary:hover{
    background-color: black;
}
.btn-outline-secondary:active{
    background-color: black;
}
</style>

<script>

</script>