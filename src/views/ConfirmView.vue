<template>
  <b-container class="py-5 text-center">
    <b-icon icon="check-circle-fill" variant="success" font-scale="3"></b-icon>
    <p class="lead mt-3">
      A Confirmation Email has been sent to <br />
      <strong>{{ email }}</strong>
    </p>
    <p>We look forward to seeing you soon!</p>

    <p>To make another appointment click here </p>

    <b-button variant="primary" @click="$router.push('/book')">Book Another</b-button>

    <p>Don’t  hesitate to  contact us today for any further questions.</p>

  </b-container>
</template>

<script>
export default {
  computed: {
    name() {
      return this.$route.query.name || 'Guest'
    },
    email() {
      return this.$route.query.email || 'your email'
    }
  }
}
</script>

<style scope>


</style>

