<template>
  <b-container class="py-5 text-center">
    <b-icon icon="check-circle-fill" variant="success" font-scale="3"></b-icon>
    <h2 class="mt-3 text-success">Appointment Confirmed!</h2>
    <p class="lead mt-3">
      Thanks <strong>{{ name }}</strong> for booking with us!<br />
      A confirmation has been sent to <strong>{{ email }}</strong>.
    </p>
    <p>Your appointment has been successfully booked.</p>

    <b-button variant="primary" @click="$router.push('/book')">Book Another</b-button>

    <b-button variant="primary" @click="$router.push('/')">Home Page</b-button>

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

