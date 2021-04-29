<template>
  <div>
    <my-form :user="selectedUser"/>

    <h1>Users</h1>
    <button v-for="user in users" @click="selectedUser = user">{{user.firstname}}</button>
  </div>
</template>

<script>
import MyForm from '@/components/MyForm'

export default {
  name: 'App',

  components: { MyForm },

  data () {
    return {
      selectedUser: {
        firstname: ''
      },
      users: [
        { firstname: 'User1' },
        { firstname: 'User2' },
        { firstname: 'User3' }
      ]
    }
  }
}
</script>
