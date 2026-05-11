<template>
  <div class="how-it-works" id="cara-kerja">
    <div class="section-title">
      <i class="fas fa-sync-alt"></i>
      Cara Kerja Second Chance Market
    </div>

    <div class="steps">

      <div class="step">
        <div class="step-number">1</div>

        <h3>📦 Posting Barang</h3>

        <p>
          Upload barang bekasmu lengkap dengan
          harga dan kategori.
        </p>
      </div>

      <div class="step">
        <div class="step-number">2</div>

        <h3>💬 Negosiasi & Chat</h3>

        <p>
          Pembeli menghubungi via chat internal
          untuk tawar menawar.
        </p>
      </div>

      <div class="step">
        <div class="step-number">3</div>

        <h3>✅ Transaksi Aman</h3>

        <p>
          Kesepakatan harga,
          barang diambil/dikirim (simulasi).
        </p>
      </div>

      <div class="step">
        <div class="step-number">4</div>

        <h3>🌟 Beri Rating</h3>

        <p>
          Bangun reputasi sebagai penjual terpercaya
          di lingkungan kampus.
        </p>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'HowItWorks',

  mounted() {
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if(entry.isIntersecting) {
          entry.target.style.opacity = "1"
          entry.target.style.transform = "translateY(0)"
        }
      })
    }, { threshold: 0.1 })

    document.querySelectorAll('.step').forEach(el => {
      el.style.opacity = "0"
      el.style.transform = "translateY(20px)"
      el.style.transition = "0.5s ease-out"
      observer.observe(el)
    })
  }
}
</script>