<template>
  <b-container>
    <b-row>
      <UserData />
      <b-col>
        <nuxt-link to="/">Back to Form</nuxt-link>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import UserData from '@/components/User/UserData'

export default {
  name: 'index',
  components: { UserData },
}
</script>

<style scoped></style>
