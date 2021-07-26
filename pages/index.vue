<template>
  <b-container fluid>
    <b-row>
      <b-col>
        <!--        User Data form-->
        <UserForm />
        <nuxt-link to="/userdata">user data</nuxt-link>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import UserForm from '@/components/User/UserForm'
export default {
  components: { UserForm },
  data() {
    return {}
  },
}
</script>
