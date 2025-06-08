<template>
  <div>
    <b-form @submit="onSubmit" @reset="onReset" v-if="show">
      <!-- Name -->
      <b-form-group label="Full Name:" label-for="name-input">
        <b-form-input
          id="name-input"
          v-model="form.name"
          type="text"
          placeholder="Enter your full name"
          required
        ></b-form-input>
      </b-form-group>

      <!-- Email -->
      <b-form-group label="Email Address:" label-for="email-input">
        <b-form-input
          id="email-input"
          v-model="form.email"
          type="email"
          placeholder="Enter your email"
          required
        ></b-form-input>
      </b-form-group>

      <!-- Phone Number -->
      <b-form-group label="Phone Number:" label-for="phone-input">
        <b-form-input
          id="phone-input"
          v-model="form.phone"
          type="tel"
          placeholder="Enter your phone number"
          required
        ></b-form-input>
      </b-form-group>

      <!-- Service -->
      <b-form-group label="Service:" label-for="service-input">
        <b-form-select
          id="service-input"
          v-model="form.service"
          :options="serviceOptions"
          required
        ></b-form-select>
      </b-form-group>

      <!-- Date -->
      <b-form-group label="Appointment Date:" label-for="date-input">
        <b-form-input
          id="date-input"
          v-model="form.date"
          type="date"
          required
        ></b-form-input>
      </b-form-group>

      <!-- Time -->
      <b-form-group label="Appointment Time:" label-for="time-input">
        <b-form-input
          id="time-input"
          v-model="form.time"
          type="time"
          required
        ></b-form-input>
      </b-form-group>

      <!-- Extra Notes -->
      <b-form-group label="Additional Notes:" label-for="notes-input">
        <b-form-textarea
          id="notes-input"
          v-model="form.notes"
          placeholder="Enter any additional information..."
          rows="3"
          max-rows="6"
        ></b-form-textarea>
      </b-form-group>

      <!-- Submit and Reset Buttons -->
      <b-button type="submit" variant="primary">Submit</b-button>
      <b-button type="reset" variant="danger" class="ml-2">Reset</b-button>
    </b-form>

    <!-- Form Output -->
    <b-card class="mt-3" header="Form Data Result">
      <pre class="m-0">{{ form }}</pre>
    </b-card>
  </div>
</template>

<script>
export default {
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
        { text: 'Select A Service', value: null, disabled: true },
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
      alert('Appointment submitted:\n' + JSON.stringify(this.form, null, 2))
      console.log("Form submitted:", this.form)
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
/* Add any scoped CSS styles you want */
</style>
