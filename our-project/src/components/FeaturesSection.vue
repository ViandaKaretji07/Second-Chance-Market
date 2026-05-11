<template>
  <div class="features" id="fitur">
    <div class="section-title">
      <i class="fas fa-star-of-life"></i>
      Fitur Andalan untuk Mahasiswa
    </div>

    <div class="feature-grid">

      <div class="feature-card">
        <div class="feature-icon">
          <i class="fas fa-box-open"></i>
        </div>

        <h3>Post Barang + Kategori</h3>

        <p>
          Upload foto, deskripsi, harga, dan pilih kategori
          (Elektronik, Furnitur, Buku, dll).
        </p>
      </div>

      <div class="feature-card">
        <div class="feature-icon">
          <i class="fas fa-comment-dots"></i>
        </div>

        <h3>Chat Penjual & Pembeli</h3>

        <p>
          Komunikasi langsung, nego harga,
          tanya kondisi barang secara realtime.
        </p>
      </div>

      <div class="feature-card">
        <div class="feature-icon">
          <i class="fas fa-heart"></i>
        </div>

        <h3>Wishlist & Simpan Barang</h3>

        <p>
          Simpan barang incaran, akses kapan saja,
          dan bandingkan harga.
        </p>
      </div>

      <div class="feature-card">
        <div class="feature-icon">
          <i class="fas fa-plane-departure"></i>
        </div>

        <h3>Titip Jual Saat Pulang</h3>

        <p>
          Jadwalkan penjualan barang sebelum mudik,
          buyer bisa pre-order!
        </p>
      </div>

      <div class="feature-card">
        <div class="feature-icon">
          <i class="fas fa-cubes"></i>
        </div>

        <h3>Bundling "Paket Anak Kos"</h3>

        <p>
          Beli kasur + meja + lampu jadi satu paket,
          lebih murah & praktis.
        </p>
      </div>

      <div class="feature-card">
        <div class="feature-icon">
          <i class="fas fa-chart-line"></i>
        </div>

        <h3>Simulasi Marketplace</h3>

        <p>
          Platform pembelajaran interaktif
          untuk memahami alur jual beli digital.
        </p>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'FeaturesSection',

  mounted() {
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if(entry.isIntersecting) {
          entry.target.style.opacity = "1"
          entry.target.style.transform = "translateY(0)"
        }
      })
    }, { threshold: 0.1 })

    document.querySelectorAll('.feature-card').forEach(el => {
      el.style.opacity = "0"
      el.style.transform = "translateY(20px)"
      el.style.transition = "0.5s ease-out"
      observer.observe(el)
    })
  }
}
</script>