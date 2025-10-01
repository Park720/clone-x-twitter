<template>
  <input type="text" placeholder="'Email'" v-model="email"/>
  <input type="password" placeholder="'Password'" v-model="password"/>

  <button>Login</button>
  <div>
    계정이 없으신가요?
    <span>가입하기</span>
  </div>
</template>

<script>
export default {
    name: "LoginPage",
    data() {
        return {
            email: "",
            password: ""
        };
    },
    methods: {
    login() {
            console.log(`Email: ${this.email}, Password: ${this.password}`);
    },  
}

}
</script>

<style>

</style>