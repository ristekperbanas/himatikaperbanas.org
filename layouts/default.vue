<template>
  <div class="center examplex">
    <vs-navbar
      v-model="active"
      style="height: 500px; z-index: -1;"
      text-white
      :color="active"
      not-line
      center-collapsed
    >
      <div style="margin-right: 500px;">
        <!-- <img src="@/assets/image/icon.jpeg" width="80" alt="" /> -->
        <svg
          style="margin-top: 20px;"
          width="40"
          height="40"
          viewBox="0 0 16 16"
          class="bi bi-building"
          fill="currentColor"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            fill-rule="evenodd"
            d="M14.763.075A.5.5 0 0 1 15 .5v15a.5.5 0 0 1-.5.5h-3a.5.5 0 0 1-.5-.5V14h-1v1.5a.5.5 0 0 1-.5.5h-9a.5.5 0 0 1-.5-.5V10a.5.5 0 0 1 .342-.474L6 7.64V4.5a.5.5 0 0 1 .276-.447l8-4a.5.5 0 0 1 .487.022zM6 8.694L1 10.36V15h5V8.694zM7 15h2v-1.5a.5.5 0 0 1 .5-.5h2a.5.5 0 0 1 .5.5V15h2V1.309l-7 3.5V15z"
          />
          <path
            d="M2 11h1v1H2v-1zm2 0h1v1H4v-1zm-2 2h1v1H2v-1zm2 0h1v1H4v-1zm4-4h1v1H8V9zm2 0h1v1h-1V9zm-2 2h1v1H8v-1zm2 0h1v1h-1v-1zm2-2h1v1h-1V9zm0 2h1v1h-1v-1zM8 7h1v1H8V7zm2 0h1v1h-1V7zm2 0h1v1h-1V7zM8 5h1v1H8V5zm2 0h1v1h-1V5zm2 0h1v1h-1V5zm0-2h1v1h-1V3z"
          />
        </svg>
        <h2
          style="display: flex; margin-top: -40px; margin-left: 60px;"
          class="poppins"
        >
          Himatika Perbanas
        </h2>
      </div>
      <div style="margin-top: 10px;">
        <vs-navbar-item
          id="primary"
          class="poppins"
          :active="active == 'primary'"
        >
          Home
        </vs-navbar-item>
        <vs-navbar-item
          id="danger"
          class="poppins"
          :active="active == 'danger'"
        >
          News
        </vs-navbar-item>
        <vs-navbar-item id="dark" class="poppins" :active="active == 'dark'">
          Store
        </vs-navbar-item>
        <vs-navbar-item
          id="success"
          class="poppins"
          :active="active == 'success'"
        >
          Jobs
        </vs-navbar-item>
      </div>
    </vs-navbar>
    <div class="square">
      <div class="child" style="margin-top: 200px;">
        <center>
          <vs-row>
            <vs-col vs-type="flex" vs-justify="center" vs-align="center" w="6">
              <h1
                class="poppins"
                style="max-width: 450px; text-align: left; color: white; position: relative; z-index: 1;"
              >
                <!-- Himpunan Mahasiswa Teknik Informatika Perbanas -->
                Selamat datang di Website Himatika Perbanas.
              </h1>
            </vs-col>
            <vs-col vs-type="flex" vs-justify="center" vs-align="center" w="6">
            </vs-col>
          </vs-row>
        </center>
        <nuxt />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data: () => ({
    active: 'primary'
  })
}
</script>
<style>
@import url('https://fonts.googleapis.com/css?family=Poppins:700&display=swap');
@import url('https://fonts.googleapis.com/css?family=DM+Sans&display=swap');

.poppins {
  font-family: 'Poppins', sans-serif !important;
}
.sans {
  font-family: 'DM Sans', sans-serif !important;
}

.conts {
  margin: 0 auto;
  max-width: 1280px;
  width: 80%;
}
</style>
