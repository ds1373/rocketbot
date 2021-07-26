<template>
  <!--  <Tutorial/>-->
  <b-container fluid>
    <b-row>
      <b-col>
        <h1>form</h1>
        <!--        User Data form-->
        <b-form @submit.prevent="onSubmit">
          <b-col>
            name
            <b-input v-model="form.name">name</b-input>
          </b-col>
          <b-col>
            family
            <b-input v-model="form.family">family</b-input>
          </b-col>
          <b-col>
            address
            <b-input v-model="form.address">address</b-input>
          </b-col>
          <b-button type="submit">submit</b-button>
        </b-form>
        <nuxt-link to="/userdata">user data</nuxt-link>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  data() {
    return {
      form: {
        name: '',
        family: '',
        address: '',
      },
    }
  },
  methods: {
    onSubmit() {
      localStorage.setItem('userData', JSON.stringify(this.form))
    },
  },
}
</script>
