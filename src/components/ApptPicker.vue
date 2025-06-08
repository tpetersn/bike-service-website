<template>
  <div>
    <h2>Complete the following to make an appointment.</h2>
    <b-form @submit="onSubmit" @reset="onReset" v-if="show" class="mt-5">
      <!-- Name -->
      <b-form-group label="Full Name:" label-for="name-input" label-cols-sm="4"
  label-cols-lg="3"
  content-cols-sm
  content-cols-lg="7">
        <b-form-input
          id="name-input"
          v-model="form.name"
          type="text"
          placeholder="Enter your full name"
          required
        ></b-form-input>
      </b-form-group>

      <!-- Email -->
      <b-form-group label="Email Address:" label-for="email-input" label-cols-sm="4"
  label-cols-lg="3"
  content-cols-sm
  content-cols-lg="7">
        <b-form-input
          id="email-input"
          v-model="form.email"
          type="email"
          placeholder="Enter your email"
          required
        ></b-form-input>
      </b-form-group>

      <!-- Phone Number -->
      <b-form-group label="Phone Number:" label-for="phone-input" label-cols-sm="4"
  label-cols-lg="3"
  content-cols-sm
  content-cols-lg="7">
        <b-form-input
          id="phone-input"
          v-model="form.phone"
          type="tel"
          placeholder="Enter your phone number"
          required
        ></b-form-input>
      </b-form-group>

      <!-- Service -->
      <b-form-group label="Service:" label-for="service-input" label-cols-sm="4"
  label-cols-lg="3"
  content-cols-sm
  content-cols-lg="7">
        <b-form-select
          id="service-input"
          v-model="form.service"
          :options="serviceOptions"
          required
        ></b-form-select>
      </b-form-group>

      <!-- Date -->
      <b-form-group label="Appointment Date:" label-for="date-input" label-cols-sm="4"
                    label-cols-lg="3"
                    content-cols-sm
                    content-cols-lg="7">
        <b-form-input
          id="date-input"
          v-model="form.date"
          type="date"
          required
        ></b-form-input>
      </b-form-group>

      <!-- Time -->
      <b-form-group label="Appointment Time:" label-for="time-input" label-cols-sm="4"
                    label-cols-lg="3"
                    content-cols-sm
                    content-cols-lg="7">
        <b-form-input
          id="time-input"
          v-model="form.time"
          type="time"
          required
        ></b-form-input>
      </b-form-group>

      <!-- Extra Notes -->
      <b-form-group label="Additional Notes:" label-for="notes-input" label-cols-sm="4"
                    label-cols-lg="3"
                    content-cols-sm
                    content-cols-lg="7">
        <b-form-textarea
          id="notes-input"
          v-model="form.notes"
          placeholder="Enter any additional information..."
          rows="3"
          max-rows="6"
        ></b-form-textarea>
      </b-form-group>

      <div class="d-flex justify-content-center">
        <b-button type="submit" variant="primary" style="width: 20rem">Submit</b-button>
      </div>
    </b-form>
  </div>
</template>

<script>
import {BButton} from "bootstrap-vue-next";

export default {
  components: {BButton},
  data() {
    return {
      form: {
        name: '',
        email: '',
        phone: '',
        service: '',
        date: '',
        time: '',
        notes: ''
      },
    serviceOptions: [
        { text: 'Select A Service', value: "", disabled: true },
        'Tire Repair',
        'Inner Tube Repair',
        'Gear Replacement',
        'Gear Adjustment',
        'Brake Pad Repair',
        'Brake Cable Repair',
        'Chain Tensioning',
        'Chain Repair',
        'Full Maintenance'
      ],
      show: true
    }
  },
  methods: {
    onSubmit(event) {
      event.preventDefault()
      this.$router.push({
        name: 'confirm',
        query: this.form
      })


    },
    onReset(event) {
      event.preventDefault()
      this.form = {
        name: '',
        email: '',
        phone: '',
        service: null,
        date: '',
        time: '',
        notes: ''
      }
      this.show = false
      this.$nextTick(() => {
        this.show = true
      })
    }
  }
}
</script>

<style scoped>
.b-form-group {
  /* Setting the margin-bottom makes the BFormGroup act more like BS4/BSVN */
  margin-bottom: 1rem;
}
</style>
