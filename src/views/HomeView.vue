<script setup>
import TheWelcome from '../components/TheWelcome.vue'
import {BButton} from "bootstrap-vue-next";
import IconCalendar from "@/components/icons/IconCalendar.vue";
</script>

<template>
  <main>
<!--    <TheWelcome />-->
    <div class="container">
      <div class="row mb-1">
        <div class="py-5 my-5 text-center">
          <div class="mx-auto"><h2>Rated the best bike repair shop in Ottawa</h2></div>
          <BButton><IconCalendar/> <span>Book An Appointment Today!</span></BButton>
        </div>
      </div>
      <div class="row mb-2 text-center">
        <div class="col-md-6 themed-grid-col">
          <div class="feature col">
            <h3 class="fs-2 text-body-emphasis">Customer Driven</h3>
            <p>The Bike Doctor prioritizes fuly transparent communication, fair pricing, and friendly, knowledgeable support for cyclists of all levels.</p>
          </div>
        </div>
        <div class="col-md-6 themed-grid-col">
          <div class="col">
            <h2>Relentless Work Ethics</h2>
            <p>The shop runs on grit.</p>
          </div>
          <div class="row">
            <div class="feature col-md-6">
              <p>Whether it’s a simple tune-up or a complex overhaul, every job gets full attention and care.</p>
            </div>
            <div class="col-md-6">
              <p>The team stays late when needed, goes the extra mile to find rare parts, and never cuts corners.</p>
            </div>
            </div>
        </div>
      </div>
    </div>
  </main>
</template>
