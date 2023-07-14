<template>
  <div class="about">
    <h1>Register Pengguna Baru</h1>
    <p>ganti warna tema : </p>
    <v-layout>
      <v-flex>
        <v-btn outlined color="#1976D2" @click="changeTheme('#1976D2')">
          Warna Biru
        </v-btn>
      </v-flex>
      <v-flex>
        <v-btn outlined color="#95ff00" @click="changeTheme('#95ff00')">
          Warna Hijau
        </v-btn>
      </v-flex>
      <v-flex>
        <v-btn outlined color="#ff7b00" @click="changeTheme('#ff7b00')">
          Warna Orange
        </v-btn>
      </v-flex>
      <v-flex>
        <v-btn outlined @click="changeDark()">
          Gelap Terang
        </v-btn>
      </v-flex>
    </v-layout>
    <v-text-field
      label="Masukkan Nama Anda"
      placeholder="Adam"
      outlined
    ></v-text-field>
    <v-text-field
      label="Masukkan Email Anda"
      placeholder="adam@mail.com"
      outlined
    ></v-text-field>
    <v-text-field
      label="Masukkan Password Anda"
      placeholder="adam_123"
      outlined
    ></v-text-field>
  </div>
</template>

<script>
export default {
  methods: {
    changeTheme(color) {
      this.$vuetify.theme.themes.light.primary = color
    },
    changeDark() {
      this.$vuetify.theme.dark = !this.$vuetify.theme.dark
    }
  }
}
</script>
