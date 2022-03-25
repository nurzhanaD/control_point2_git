<template>
    <div class="registerView">
        <h1>Create An Account</h1>
        <form class="card">
        <div class="form-group">
            <label for="InputEmail1" class="form-label mt-4">Email address</label>
            <input type="email" class="form-control" id="InputEmail1" aria-describedby="emailHelp" placeholder="Enter email" v-model="state.email">
            <span v-if="v$.email.$error">{{v$.email.$errors[0].$message}}</span>
        </div>
        <div class="form-group">
            <label for="InputPassword1" class="form-label mt-4">Password</label>
            <input type="password" class="form-control" id="InputPassword1" placeholder="Password" v-model="state.password.password">
            <span v-if="v$.password.password.$error">{{v$.password.password.$errors[0].$message}}</span>
        </div>
        <div class="form-group">
            <label for="ConfirmInputPassword1" class="form-label mt-4">Confirm Password</label>
            <input type="password" class="form-control" id="ConfirmInputPassword1" placeholder="Confirm Password" v-model="state.password.confirm">
            <span v-if="v$.password.confirm.$error">{{v$.password.confirm.$errors[0].$message}}</span>
        </div>
        <div class="form-group">
            <label for="Select1" class="form-label mt-4">User status</label>
            <select class="form-select" id="Select1">
                <option>user</option>
                <option>admin</option>
            </select>
        </div>
        <br>
        <button @click="submitForm" type="submit" class="btn btn-outline-secondary">Create</button>
    </form>
        <router-link to="/" style="font-size:1.4rem;">Go to Home.</router-link>
        <span style="font-size:1.4rem;">Already have an account? <router-link to="/login">Login here.</router-link></span>
    </div>
</template>

<script>
import useValidate from '@vuelidate/core';
import { required,email, minLength, sameAs } from '@vuelidate/validators';
import {reactive, computed} from 'vue';
export default {
    setup(){
        const state = reactive({
            email:'',
             password:{
                 password:'',
                 confirm:''
             }
        })

        const rules = computed(() => {
            return {
                email:{required, email },
                password:{
                    password:{required,minLength: minLength(6)},
                    confirm:{required, sameAs: sameAs(state.password.password)}
                }
            }
        })

        const v$ = useValidate(rules, state)
        return {
            state,
            v$
        }
    },
    methods:{
        submitForm() {
            this.v$.$validate()
        }
    }
}
</script>

<style scoped>
.registerView{
    margin:0;
    padding:0;
    height:100vh;
    display:flex;
    justify-content: center;
    align-items: center;
    background-color: orange;
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

