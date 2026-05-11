<template>
  <section class="testimoni">
    <h2 class="section-title">
      Apa Kata Mereka?
    </h2>

    <div class="testi-card">
      <p>
        "Aku bisa menjual lemari bekas sebelum pulang kampung!"
      </p>

      <h4>— Dina, Informatika 2022</h4>
    </div>

    <div class="btn-wrapper">
      <button class="btn-primary" @click="redirect">
        Coba Sekarang
      </button>
    </div>
  </section>
</template>

<script setup>
const redirect = () => {
  alert("Buka Marketplace")
}
</script>

<style scoped>
.testimoni {
  background: white;
  padding: 60px 8%;
  text-align: center;
}

.testi-card {
  background: #f5fbf8;
  max-width: 600px;
  margin: auto;
  padding: 30px;
  border-radius: 30px;
}

.btn-wrapper {
  margin-top: 30px;
}

.btn-primary {
  background: #1e6f5c;
  color: white;
  border: none;
  padding: 14px 30px;
  border-radius: 40px;
  cursor: pointer;
}
</style>