<template>
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
</template>

<script>
export default {
  name: 'UserForm',
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

<style scoped></style>
