<template>
  <b-container>
    <b-row>
      <b-col>
        <!--        User data -->
        <h1>User Data</h1>
        <ul>
          <li>Name: {{ getForm.name }}</li>
          <li>Family: {{ getForm.family }}</li>
          <li>Address: {{ getForm.address }}</li>
        </ul>
        <nuxt-link to="/">Back to Form</nuxt-link>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  name: 'index',
  computed: {
    getForm() {
      return localStorage.getItem('userData')
        ? JSON.parse(localStorage.getItem('userData'))
        : {}
    },
  },
}
</script>

<style scoped></style>
