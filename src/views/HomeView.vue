<script setup>
import {BButton} from "bootstrap-vue-next";
import IconCalendar from "@/components/icons/IconCalendar.vue";
</script>

<template>
  <main>
    <div class="container">
      <div class="row mb-1">
        <div class="py-5 my-5 text-center">
          <div class="mx-auto"><h2>Rated the best bike repair shop in Ottawa</h2></div>
          <BButton><RouterLink to="/book"><IconCalendar/> <span>Book An Appointment Today!</span></RouterLink></BButton>
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
    <!-- -->

      <div class="row mb-4">
      <!-- Text Column -->
        <div class="col-md-6">
          <h3 class="text-center service">Services we offer</h3>
          <p class="text-center">
            Our services are a fixed rate. <br>
            The cost for each specific service can be found below.
          </p>
          <div class="text-left list">
            <ul>
                <li class="list-group-item d-flex justify-content-between align-items-center">
                  Tire Repair
                  <span class="badge bg-primary rounded-pill"> $20 </span>
                </li>
                <li class="list-group-item d-flex justify-content-between align-items-center">
                  Inner Tube Repair
                  <span class="badge bg-primary rounded-pill"> $18 </span>
                </li>
                <li class="list-group-item d-flex justify-content-between align-items-center">
                  Gear Replacement
                  <span class="badge bg-primary rounded-pill"> $17.50 </span>
                </li>
                <li class="list-group-item d-flex justify-content-between align-items-center">
                  Brake Pad Repair
                  <span class="badge bg-primary rounded-pill"> $12 </span>
                </li>
                <li class="list-group-item d-flex justify-content-between align-items-center">
                  Brake Cable Repair
                  <span class="badge bg-primary rounded-pill"> $18 </span>
                </li>
                <li class="list-group-item d-flex justify-content-between align-items-center">
                  Chain Tensioning
                  <span class="badge bg-primary rounded-pill"> $15 </span>
                </li>
                <li class="list-group-item d-flex justify-content-between align-items-center">
                  Chain Repair
                  <span class="badge bg-primary rounded-pill"> $30 </span>
                </li>
                <li class="list-group-item d-flex justify-content-between align-items-center">
                  Full Maintenance
                  <span class="badge bg-primary rounded-pill"> $50 </span>
                </li>
            </ul>
          </div>

        </div>

      <!-- Image Column -->
      <div class="col-md-6 d-flex align-items-center">
        <BImg
          src="/images/bike-repair-shop-2.png"
          fluid
          alt="Vertical image"
          class="w-100 rounded pic-1"
        />
        </div>
      </div>

      <div class="row mb-5">
        <div class="col-md-6 d-flex align-items-center">
          <BImg
            src="/images/bike-repair-3.png"
            fluid
            alt="Horizontal image"
            class="w-100 rounded pic-2"
          />
        </div>

        <div class="col-md-6 text-center">
          <h3 class="tech">
            Tool Tech <br>
          </h3>
          <p class="tech-info">
            The Bike Doctor uses advanced tools such as digital torque wrenches, laser-guided wheel alignment, hydraulic brake bleeding stations, and drivetrain alignment sensors to pinpoint problems, allowing for the most accurate repairs.
          </p>

        </div>

      </div>


      <div class="text-center">
        <h3>
          We Value Communication <br>
        </h3>
        <p>
          Clients with bikes in the shop will receive digital service reports with photos, status notifications via app or SMS, and can approve quotes online for services not listed. The shop features a semi-automated workbench system that tracks service orders, uses barcodes to log parts, and syncs with a digital inventory management
        </p>

      </div>

    </div>
  </main>
</template>


<style scoped>


.pic-1{
  width: 100%;
  height: 200px;
  object-fit: cover;
  display: block;
  border: 2px solid white;

}
.pic-2{
  width: 100%;
  height: 200px;
  object-fit: cover;
  display: block;
  border: 2px solid white;
}

@media (min-width: 1024px) {
  .service{
  margin-top:35px;
}
.list{
  margin-top: 100px;
}
.tech{
margin-top:110px
}
.tech-info {
  margin-top:35px
}

  .pic-1 {
    height:500px;

  }
  .pic-2{
    height: auto;
  }


}
</style>
