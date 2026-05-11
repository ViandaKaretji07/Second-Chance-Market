<template>
  <div class="navbar">
    <div class="logo">
      <i class="fas fa-leaf"></i> Second Chance Market
    </div>

    <div class="nav-links">
      <a href="#">Beranda</a>
      <a href="#fitur">Fitur</a>
      <a href="#cara-kerja">Panduan</a>

      <a href="#" @click.prevent="goToMarket" class="btn-masuk">
        <i class="fas fa-store"></i> Masuk Marketplace
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Navbar',

  methods: {
    goToMarket() {
      alert(
        "✨ Menuju ke Marketplace Second Chance Market ✨\n(Dalam implementasi nyata, ini akan membuka halaman utama marketplace dengan semua fitur: Posting, Chat, Wishlist, Bundling, Titip Jual)"
      )

      window.open("#", "_self")
    }
  }
}
</script>