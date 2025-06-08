<template>
  <div id="footer">
    <footer class="text-white mt-auto">
      <!-- Grid container -->
      <div class="container p-4">
        <div class="row justify-content-between">
          <section class="col-4">
            <h2>The Bike Doctor <IconBike /></h2>
            <div><IconMapMarker />  1320 Somerset St. W</div>
            <div><IconPhone /> 613-548-9210</div>
            <div><IconMail /> service@thebikedoctor.ca</div>
          </section>
          <section class="col-4 ">
            <h2 class="text-center">Hours</h2>
            <div class="border border-dashed">
              <div class="p-2">Monday-Thursday: 10:00-20:00</div>
              <div class="p-2">Friday-Saturday: 09:00-17:00</div>
              <div class="p-2">Sunday: Closed</div>
            </div>
          </section>
        </div>
      </div>
      <!-- Grid container -->
    </footer>
  </div>
</template>

<style scoped>
footer {
  position: sticky;
  width: 100%;
}

footer section svg {
  fill: white;
}

</style>
<script setup>
import IconBike from "@/components/icons/IconBike.vue";
import IconMapMarker from "@/components/icons/IconMapMarker.vue";
import IconPhone from "@/components/icons/IconPhone.vue";
import IconMail from "@/components/icons/IconMail.vue";
</script>
