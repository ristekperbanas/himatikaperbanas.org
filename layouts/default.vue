<template>
  <div class="center examplex">
    <vs-navbar
      v-model="navbarDesk"
      class="navbar-desktop"
      style="height: 500px; z-index: -1;"
      text-white
      :color="navbarDesk"
      not-line
      center-collapsed
    >
      <div style="margin-right: 600px;">
        <!-- <img src="@/assets/image/icon.jpeg" width="80" alt="" /> -->
        <svg
          style="margin-top: 30px;"
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
          style="display: flex; margin-top: -38px; margin-left: 60px;"
          class="open-sans"
        >
          Himatika Perbanas
        </h2>
      </div>
      <div style="margin-top: 10px;">
        <vs-navbar-item
          id="primary"
          class="poppins"
          :active="navbarDesk == 'primary'"
          @click="NavChange('home')"
        >
          Home
        </vs-navbar-item>
        <vs-navbar-item
          id="danger"
          class="poppins"
          :active="navbarDesk == 'danger'"
          @click="NavChange('news')"
        >
          News
        </vs-navbar-item>
        <vs-navbar-item
          id="dark"
          class="poppins"
          :active="navbarDesk == 'dark'"
          @click="NavChange('showcase')"
        >
          Showcase
        </vs-navbar-item>
        <vs-navbar-item
          id="success"
          class="poppins"
          :active="navbarDesk == 'success'"
          @click="NavChange('jobs')"
        >
          Jobs
        </vs-navbar-item>
      </div>
    </vs-navbar>

    <vs-navbar
      v-model="navbarMob"
      shadow
      square
      center-collapsed
      text-white
      :color="navbarColor"
      class="navbar-mobile"
      style="display: none; height: 350px; z-index: -1;"
    >
      <template #left>
        <vs-button
          style="background-color: white; margin-top: 15px;"
          flat
          icon
          @click="activeSidebar = !activeSidebar"
        >
          <svg
            :color="navbarColor"
            width="20"
            height="20"
            viewBox="0 0 16 16"
            class="bi bi-arrow-right"
            fill="currentColor"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              fill-rule="evenodd"
              d="M1 8a.5.5 0 0 1 .5-.5h11.793l-3.147-3.146a.5.5 0 0 1 .708-.708l4 4a.5.5 0 0 1 0 .708l-4 4a.5.5 0 0 1-.708-.708L13.293 8.5H1.5A.5.5 0 0 1 1 8z"
            />
          </svg>
        </vs-button>
      </template>
    </vs-navbar>
    <vs-sidebar v-model="navbarMob" absolute :open.sync="activeSidebar">
      <template #logo>
        <svg
          width="40"
          height="40"
          style="margin-left: -30px; color: #1c59f6;"
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
        <h3 style="margin-left: 5px; color: #1c59f6;" class="open-sans">
          Himatika <br />Perbanas
        </h3>
      </template>
      <vs-sidebar-item id="home">
        <a href="/" style="text-decoration: none; color: #1c59f6;">Home</a>
      </vs-sidebar-item>
      <vs-sidebar-item id="news">
        <a href="/news" style="text-decoration: none; color: #1c59f6;">News</a>
      </vs-sidebar-item>
      <vs-sidebar-item id="showcase">
        <a href="/showcase" style="text-decoration: none; color: #1c59f6;"
          >Showcase</a
        >
      </vs-sidebar-item>
      <vs-sidebar-item id="jobs">
        <a href="/jobs" style="text-decoration: none; color: #1c59f6;">Jobs</a>
      </vs-sidebar-item>
    </vs-sidebar>
    <div class="square">
      <div class="child" style="margin-top: 150px;">
        <center class="banner-desktop">
          <vs-row>
            <vs-col vs-type="flex" vs-justify="center" vs-align="center" w="6">
              <h1
                class="open-sans"
                style="max-width: 450px; text-align: left; color: white; position: relative; z-index: 1;"
              >
                {{ title }}
              </h1>
              <p
                class="poppins"
                style="max-width: 450px; text-align: left; color: white;"
              >
                {{ desc }}
              </p>
              <div
                style="margin-top: 25px; max-width: 460px; text-align: left;"
              >
                <vs-button
                  :color="btnColor"
                  size="large"
                  flat
                  style="padding: 5px; background-color: white;"
                >
                  {{ btnText }}
                </vs-button>
              </div>
            </vs-col>
            <vs-col vs-type="flex" vs-justify="center" vs-align="center" w="6">
              <svg
                width="250"
                height="250"
                style="color: white;"
                viewBox="0 0 16 16"
                :class="icon"
                fill="currentColor"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path fill-rule="evenodd" :d="path1" />
                <path :d="path2" />
              </svg>
            </vs-col>
          </vs-row>
        </center>

        <div class="banner-mobile" style="margin-top: -55px; display:none;">
          <h1 class="open-sans" style="text-align: center; color: white;">
            {{ title }}
          </h1>

          <p class="poppins" style="text-align: center; color: white;">
            {{ desc }}
          </p>

          <!-- <center>
            <vs-button
              active
              size="large"
              border
              style="margin-top: 30px; padding: 5px; border: 2px solid white;"
            >
              View more
            </vs-button>
          </center> -->
        </div>
        <nuxt />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data: () => ({
    navbarDesk: 'primary',
    navbarMob: 'home',
    active: 0,
    navbarColor: 'primary',
    activeSidebar: false,
    btnColor: 'primary',
    btnText: 'View More',
    title: 'Selamat datang di Website Himatika Perbanas',
    icon: 'bi-building',
    path1:
      'M14.763.075A.5.5 0 0 1 15 .5v15a.5.5 0 0 1-.5.5h-3a.5.5 0 0 1-.5-.5V14h-1v1.5a.5.5 0 0 1-.5.5h-9a.5.5 0 0 1-.5-.5V10a.5.5 0 0 1 .342-.474L6 7.64V4.5a.5.5 0 0 1 .276-.447l8-4a.5.5 0 0 1 .487.022zM6 8.694L1 10.36V15h5V8.694zM7 15h2v-1.5a.5.5 0 0 1 .5-.5h2a.5.5 0 0 1 .5.5V15h2V1.309l-7 3.5V15z',
    path2:
      'M2 11h1v1H2v-1zm2 0h1v1H4v-1zm-2 2h1v1H2v-1zm2 0h1v1H4v-1zm4-4h1v1H8V9zm2 0h1v1h-1V9zm-2 2h1v1H8v-1zm2 0h1v1h-1v-1zm2-2h1v1h-1V9zm0 2h1v1h-1v-1zM8 7h1v1H8V7zm2 0h1v1h-1V7zm2 0h1v1h-1V7zM8 5h1v1H8V5zm2 0h1v1h-1V5zm2 0h1v1h-1V5zm0-2h1v1h-1V3z',
    desc:
      'Lihat berbagai macam informasi seputar kami, mulai dari berita, pekerjaan dan karya dari kami.'
  }),
  methods: {
    NavChange(values) {
      if (values === 'home') {
        this.btnText = 'View more'
        this.title = 'Selamat datang di Website Himatika Perbanas'
        this.desc =
          'Lihat berbagai macam informasi seputar kami, mulai dari berita, pekerjaan dan karya dari kami.'
        this.btnColor = 'primary'
        this.icon = 'bi-building'
        this.path1 =
          'M14.763.075A.5.5 0 0 1 15 .5v15a.5.5 0 0 1-.5.5h-3a.5.5 0 0 1-.5-.5V14h-1v1.5a.5.5 0 0 1-.5.5h-9a.5.5 0 0 1-.5-.5V10a.5.5 0 0 1 .342-.474L6 7.64V4.5a.5.5 0 0 1 .276-.447l8-4a.5.5 0 0 1 .487.022zM6 8.694L1 10.36V15h5V8.694zM7 15h2v-1.5a.5.5 0 0 1 .5-.5h2a.5.5 0 0 1 .5.5V15h2V1.309l-7 3.5V15z'
        this.path2 =
          'M2 11h1v1H2v-1zm2 0h1v1H4v-1zm-2 2h1v1H2v-1zm2 0h1v1H4v-1zm4-4h1v1H8V9zm2 0h1v1h-1V9zm-2 2h1v1H8v-1zm2 0h1v1h-1v-1zm2-2h1v1h-1V9zm0 2h1v1h-1v-1zM8 7h1v1H8V7zm2 0h1v1h-1V7zm2 0h1v1h-1V7zM8 5h1v1H8V5zm2 0h1v1h-1V5zm2 0h1v1h-1V5zm0-2h1v1h-1V3z'
      } else if (values === 'news') {
        this.btnText = 'Coming Soon'
        this.title = 'Baca berita penting dan menarik seputar IT'
        this.desc =
          'Lihat berbagai macam informasi dan berita dari kami yang dapat menginspirasi kamu.'
        this.btnColor = 'danger'
        this.icon = 'bi bi-newspaper'
        this.path1 =
          'M0 2.5A1.5 1.5 0 0 1 1.5 1h11A1.5 1.5 0 0 1 14 2.5v10.528c0 .3-.05.654-.238.972h.738a.5.5 0 0 0 .5-.5v-9a.5.5 0 0 1 1 0v9a1.5 1.5 0 0 1-1.5 1.5H1.497A1.497 1.497 0 0 1 0 13.5v-11zM12 14c.37 0 .654-.211.853-.441.092-.106.147-.279.147-.531V2.5a.5.5 0 0 0-.5-.5h-11a.5.5 0 0 0-.5.5v11c0 .278.223.5.497.5H12z'
        this.path2 =
          'M2 3h10v2H2V3zm0 3h4v3H2V6zm0 4h4v1H2v-1zm0 2h4v1H2v-1zm5-6h2v1H7V6zm3 0h2v1h-2V6zM7 8h2v1H7V8zm3 0h2v1h-2V8zm-3 2h2v1H7v-1zm3 0h2v1h-2v-1zm-3 2h2v1H7v-1zm3 0h2v1h-2v-1z'
      } else if (values === 'showcase') {
        this.btnText = 'Coming Soon'
        this.title = 'Hasil karya dari anggota Himatika Perbanas'
        this.desc =
          'Lihat berbagai macam karya dari kami yang dibuat dengan sepenuh hati.'
        this.btnColor = 'dark'
        this.icon = 'bi bi-bookmark-star'
        this.path1 =
          'M2 2a2 2 0 0 1 2-2h8a2 2 0 0 1 2 2v13.5a.5.5 0 0 1-.777.416L8 13.101l-5.223 2.815A.5.5 0 0 1 2 15.5V2zm2-1a1 1 0 0 0-1 1v12.566l4.723-2.482a.5.5 0 0 1 .554 0L13 14.566V2a1 1 0 0 0-1-1H4z'
        this.path2 =
          'M7.84 4.1a.178.178 0 0 1 .32 0l.634 1.285a.178.178 0 0 0 .134.098l1.42.206c.145.021.204.2.098.303L9.42 6.993a.178.178 0 0 0-.051.158l.242 1.414a.178.178 0 0 1-.258.187l-1.27-.668a.178.178 0 0 0-.165 0l-1.27.668a.178.178 0 0 1-.257-.187l.242-1.414a.178.178 0 0 0-.05-.158l-1.03-1.001a.178.178 0 0 1 .098-.303l1.42-.206a.178.178 0 0 0 .134-.098L7.84 4.1z'
      } else if (values === 'jobs') {
        this.btnText = 'Coming Soon'
        this.title = 'Cari dan temukan pekerjaan terbaru untuk kamu'
        this.desc =
          'Lihat berbagai informasi pekerjaan yang ada sesuai dengan skill kamu.'
        this.btnColor = 'success'
        this.icon = 'bi bi-person-lines-fill'
        this.path1 =
          'M1 14s-1 0-1-1 1-4 6-4 6 3 6 4-1 1-1 1H1zm5-6a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm7 1.5a.5.5 0 0 1 .5-.5h2a.5.5 0 0 1 0 1h-2a.5.5 0 0 1-.5-.5zm-2-3a.5.5 0 0 1 .5-.5h4a.5.5 0 0 1 0 1h-4a.5.5 0 0 1-.5-.5zm0-3a.5.5 0 0 1 .5-.5h4a.5.5 0 0 1 0 1h-4a.5.5 0 0 1-.5-.5zm2 9a.5.5 0 0 1 .5-.5h2a.5.5 0 0 1 0 1h-2a.5.5 0 0 1-.5-.5z'
        this.path2 = ''
      } else {
        return false
      }
    }
  }
}
</script>
<style>
@import url('https://fonts.googleapis.com/css?family=Poppins&display=swap');
@import url('https://fonts.googleapis.com/css?family=DM+Sans&display=swap');
@import '@/assets/styles/font.css';

.open-sans {
  font-family: 'Google Sans', sans-serif !important;
}

.sans {
  font-family: 'DM Sans', sans-serif !important;
}

.poppins {
  font-family: 'Poppins', sans-serif !important;
}

.conts {
  margin: 0 auto;
  max-width: 1280px;
  width: 80%;
}

@media only screen and (max-width: 600px) {
  .navbar-desktop,
  .banner-desktop {
    display: none;
  }

  .navbar-mobile,
  .banner-mobile {
    display: block !important;
  }
}
</style>
