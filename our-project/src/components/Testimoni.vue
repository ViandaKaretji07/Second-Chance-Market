<template>
  <div class="testimoni">
    <div class="section-title">
      <i class="fas fa-quote-left"></i>
      Apa Kata Mereka?
    </div>

    <div class="testi-card">
      <i class="fas fa-star" style="color: #f5b042;"></i>
      <i class="fas fa-star" style="color: #f5b042;"></i>
      <i class="fas fa-star" style="color: #f5b042;"></i>
      <i class="fas fa-star" style="color: #f5b042;"></i>
      <i class="fas fa-star" style="color: #f5b042;"></i>

      <p style="margin: 20px 0;">
        "Aku bisa jualan lemari bekas sebelum pulang kampung!
        Fitur titip jual sangat membantu.
        Dalam 2 hari langsung laku!"
      </p>

      <h4>— Dina, Informatika 2022</h4>
    </div>

    <div style="margin-top: 35px; text-align:center;">
      <button class="btn-primary-landing" @click="goToMarket">
        <i class="fas fa-arrow-right"></i>
        Coba Sekarang — Buka Marketplace
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Testimoni',

  methods: {
    goToMarket() {
      alert(
        "✨ Menuju ke Marketplace Second Chance Market ✨\n(Dalam implementasi nyata, ini akan membuka halaman utama marketplace dengan semua fitur: Posting, Chat, Wishlist, Bundling, Titip Jual)"
      )

      window.open("#", "_self")
    }
  },

  mounted() {
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if(entry.isIntersecting) {
          entry.target.style.opacity = "1"
          entry.target.style.transform = "translateY(0)"
        }
      })
    }, { threshold: 0.1 })

    document.querySelectorAll('.testi-card').forEach(el => {
      el.style.opacity = "0"
      el.style.transform = "translateY(20px)"
      el.style.transition = "0.5s ease-out"
      observer.observe(el)
    })
  }
}
</script>