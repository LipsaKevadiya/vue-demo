<template>
<p>{{form}}</p>

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
      }
    }
  },
  methods: {
    login() {
      console.warn("login data", this.form);
    }
  }

}
</script>

<style scoped>
h1 {
  color: black
}
</style>
