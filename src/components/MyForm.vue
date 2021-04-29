<template>
  <form>
    <input v-model="form.firstname" type="text" placeholder="First Name" />
    <input type="submit" />{{ user.firstname }}
  </form>
</template>

<script>
export default {
  name: 'MyForm',

  props: [
    'user'
  ],

  data() {
    return {
      form: {
        firstname: this.user.firstname
      }
    }
  },

}
</script>
