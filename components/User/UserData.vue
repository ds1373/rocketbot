<template>
  <!--        User data -->
  <v-col>
    <h1>User Data</h1>
    <ul>
      <li>Name: {{ getForm.name }}</li>
      <li>Family: {{ getForm.family }}</li>
      <li>Address: {{ getForm.address }}</li>
    </ul>
  </v-col>
</template>

<script>
export default {
  name: 'UserData',
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
