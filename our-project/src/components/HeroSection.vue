<template>
  <div class="hero">
    <div class="hero-left animate-left">

      <h1>Barang bekasmu bukan sekadar sisa, tapi <span class="highlight">peluang baru!</span></h1>
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
      <div style=" border-radius: 48px; padding: 12px;">
        <img
          src="@/assets/image/sicantik.jpg"
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

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Baloo+2:wght@600;700;800&family=Poppins:wght@400;500;600;700&display=swap');

.hero-left h1 {
  font-family: 'Poppins', sans-serif;
  font-weight: 700;
}

.hero-left p {
  font-family: 'Poppins', sans-serif;
  font-weight: 400;
}

.btn-primary-landing,
.btn-outline-landing {
  font-family: 'Poppins', sans-serif;
  font-weight: 600;
}
</style>