<template>
<ul>
<li v-for="item in error" v-bind:key="item">{{item}} not valid</li>
</ul>

<h1>Simple Form</h1>
<label>Email :</label>
<input type="text" placeholder="Enter Email" v-model="form.email" />
<label>Password :</label>
<input type="password" placeholder="Enter Password" v-model="form.password" />

<button type="button" v-on:click="login">Login</button>

<select v-model="form.country">
  <option>India</option>
  <option>Germany</option>
  <option>Canada</option>
</select>

<h3>Technology</h3>
<label>react :</label>
<input type="checkbox" value="react" v-model="form.technology" />
<label>vue :</label>
<input type="checkbox" value="vue" v-model="form.technology" />

<h3>gender</h3>
<label>male :</label>
<input type="radio" value="male" name="male" v-model="form.gender" />
<label>female :</label>
<input type="radio" value="female" name="male" v-model="form.gender" />

</template>

<script>
export default {
  name: 'SimpleForm',
  data() {
    return {
      form: {
        email: '',
        password: '',
        country: '',
        technology: [],
        gender: ''
      },
      error:[],
    }
  },
  methods: {
    login() {
      this.error=[];
        const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
      if (!emailPattern.test(this.form.email)) {
        this.error.push('Email');
      }
      for(const item in this.form ){
        if(this.form[item] === "" || this.form[item].length === 0){
          this.error.push(item)
        }
      }
      if(this.error.length === 0){
        alert("data has been submit")
      }
      console.warn("login data", this.form , this.error);
    }
  }

}
</script>

<style scoped>
h1 {
  color: black
}
</style>
