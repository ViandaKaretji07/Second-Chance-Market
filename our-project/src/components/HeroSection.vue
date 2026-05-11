<template>
  <div class="hero">
    <div class="hero-left animate-left">
      <div class="typing-badge">
        <i class="fas fa-graduation-cap"></i> Marketplace Kampus #1
      </div>

      <h1>
        Jual & Beli
        <span class="highlight">Barang Bekas Mahasiswa</span>
        Lebih Cerdas
      </h1>

      <p>
        ✨ Second Chance Market: wujudkan ekonomi sirkular kampus.
        Dari anak kos untuk anak kos, dengan fitur titip jual pulang
        kampung, bundling hemat, dan chat langsung.
      </p>

      <div class="cta-group">
        <button class="btn-primary-landing" @click="goToMarket">
          <i class="fas fa-rocket"></i> Mulai Jelajahi
        </button>

        <button class="btn-outline-landing" @click="showDemo">
          <i class="fas fa-play-circle"></i> Lihat Demo
        </button>
      </div>
    </div>

    <div class="hero-right animate-up">
      <div style="background: #bdd9cf; border-radius: 48px; padding: 12px;">
        <img
          src="https://placehold.co/500x400/e0f0ea/2c7a5e?text=Second+Chance+Market"
          alt="Marketplace Preview"
          style="border-radius: 40px; width:100%; height: auto;"
        >
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeroSection',

  methods: {
    goToMarket() {
      alert(
        "✨ Menuju ke Marketplace Second Chance Market ✨\n(Dalam implementasi nyata, ini akan membuka halaman utama marketplace dengan semua fitur: Posting, Chat, Wishlist, Bundling, Titip Jual)"
      )

      window.open("#", "_self")
    },

    showDemo() {
      alert(
        "🎥 Demo Fitur:\n- Post barang dengan foto emoji\n- Chat realtime antar user\n- Wishlist & Titip jual\n- Bundling barang kos.\nSilakan buka marketplace untuk mencoba langsung."
      )
    }
  }
}
</script>