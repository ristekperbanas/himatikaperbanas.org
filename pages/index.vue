<template>
  <div class="app conts mob-space" style="padding-bottom: 0px;">
    <h1 class="open-sans blue-text">Tentang Kami</h1>
    <br />
    <p class="poppins" style="font-size: 20px; margin-top: -10px;">
      Himpunan Mahasiswa Teknik Informatika (Himatika) Perbanas adalah
      organisasi yang bertujuan untuk mengembangkan kualitas mahasiswa/i dari
      jurusan Teknik Informatika dan dijadikan sebagai wadah menyalurkan
      inspirasi dan aspirasi. Himatika ABFI Institute Perbanas didirikan oleh
      mahasiswa STIMIK Perbanas jurusan Teknik Informatika angkatan 2000 tetapi
      baru aktif di tahun 2002. Tanggal 16 Juli 2008 Himatika ABFI Institute
      Perbanas telah berdiri secara resmi dan disahkan oleh pihak lembaga
      sebagai salah satu Organisasi Mahasiswa (Ormawa) yang ada di ABFI
      Institute Perbanas. Visi Menjadi suatu komunitas mahasiswa yang unggul di
      dalam bidang Teknologi Informasi dan menghasilkan mahasiswa yang kreatif
      dan berkualitas dalam rangka memberikan kontribusi positif bagi masyarakat
      pad aumumnya dan sivitas akademika ABFI Institute Perbanas pada khususnya
      sesuai dengan TRI DARMA pendidikan.
    </p>
    <br />
    <h1 class="open-sans blue-text">Misi Kami</h1>
    <vs-row v-for="(misi, idx) in mission" :key="idx">
      <vs-col vs-type="flex" vs-justify="center" vs-align="center" w="6">
        <p
          class="poppins"
          style="max-width: 450px; font-size: 25px; text-align: left; position: relative; z-index: 1;"
        >
          {{ misi.title }}
        </p>
      </vs-col>
      <vs-col vs-type="flex" vs-justify="center" vs-align="center" w="6">
        <img :src="misi.image" alt="" style="width: 500px;" />
      </vs-col>
    </vs-row>

    <br />
    <br />
    <center>
      <h1 class="open-sans blue-text">What We Do</h1>
      <div v-for="(item, id) in dos" :key="id">
        <img :src="item.img" style="width: 100%;" />
        <h1 class="open-sans blue-text">{{ item.title }}</h1>
        <h3 class="poppins">{{ item.desc }}</h3>
      </div>
      <br />
      <br />
      <hr />
      <h1 class="open-sans blue-text">© 2020 Himatika Perbanas</h1>
    </center>
  </div>
</template>

<script>
import mission1 from '@/assets/image/mission1.png'
import mission2 from '@/assets/image/mission2.png'
import do1 from '@/assets/image/do1.png'
import do2 from '@/assets/image/do2.png'
import do3 from '@/assets/image/do3.png'
import do4 from '@/assets/image/do4.png'
import do5 from '@/assets/image/do5.png'
import do6 from '@/assets/image/do6.png'
export default {
  data: () => ({
    mission: [
      {
        title:
          'Menjalin Dan Mempererat Tali Silaturahmi Dan Komunikasi Serta Kerjasama Antar Mahasiswa Teknik Informatika Dan Sivitas Akademika ABFI Institute Perbanas.',
        image: mission1
      },
      {
        title:
          'Menyelenggarakan Pembelajaran Dan Pelatihan Kepada Mahasiswa Teknik Informatika Pada Khususnya Dan Masyarakat Pada Umumnya Di Bidang Teknologi Informasi.',
        image: mission2
      }
    ],
    dos: [
      {
        title: 'PELATIHAN',
        desc: 'Pelatihan untuk mengasah skill',
        img: do1
      },
      {
        title: 'SEMINAR',
        desc: 'Seminar untuk menambah pengetahuan',
        img: do2
      },
      {
        title: 'BUKA PUASA BERSAMA',
        desc: 'Menjalin silahturahmi',
        img: do3
      },
      {
        title: 'MUSYAWARAH BESAR',
        desc: 'Untuk kepentingan bersama',
        img: do4
      },
      {
        title: 'PENDIDIKAN DASAR (DIKDAS)',
        desc: 'Untuk mengenal lingkungan dan Kultur',
        img: do5
      },
      {
        title: 'SHARING IT',
        desc: 'Sharing pengalaman dan pengetahuan',
        img: do6
      }
    ]
  })
}
</script>

<style>
.app {
  margin-top: 150px;
  width: 100%;
}

.blue-text {
  color: #1c59f6;
}
</style>
