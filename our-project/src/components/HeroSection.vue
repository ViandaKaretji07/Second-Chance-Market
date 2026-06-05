<template>
  <div class="hero">
    <div class="hero-left animate-left">
      <div class="typing-badge">
         <img 
        src="@/assets/image/logo.png" 
        alt="Logo" 
        style="width: 15px; height: 15px;"
      />
        Marketplace Kampus #1
      </div>

      <h1>"Barang bekasmu bukan sekadar sisa, tapi <span class="highlight">peluang baru!</span>"</h1>
        <!-- INTEREST (I) dimasukkan di sini sebagai sub-pesan yang kuat -->
        <p><span class="highlight-interest"> Bayangkan betapa mudahnya menjual atau membeli barang bekas yang masih layak pakai, khususnya bagi mahasiswa rantau.</span> Dengan Second Chance Market, kamu bisa menemukan meja belajar, kasur, hingga peralatan dapur dengan harga ramah kantong, langsung dari sesama mahasiswa.</p>

      <div class="cta-group">
        <button class="btn-primary-landing" @click="goToMarket">
          Mulai Jelajahi
        </button>

        <button class="btn-outline-landing" @click="showDemo">
          Lihat Demo
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