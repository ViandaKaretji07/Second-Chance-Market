<template>
  <section class="hero">
    <div class="hero-left">
      <div class="typing-badge">
        <i class="fas fa-graduation-cap"></i>
        Marketplace Kampus #1
      </div>

      <h1>
        Jual & Beli
        <span class="highlight">Barang Bekas Mahasiswa</span>
        Lebih Cerdas
      </h1>

      <p>
        Second Chance Market membantu mahasiswa menjual dan membeli barang bekas dengan mudah.
      </p>

      <div class="cta-group">
        <button class="btn-primary" @click="explore">
          Mulai Jelajahi
        </button>

        <button class="btn-outline" @click="demo">
          Lihat Demo
        </button>
      </div>
    </div>

    <div class="hero-right">
      <img
        src="https://placehold.co/500x400/e0f0ea/2c7a5e?text=Second+Chance+Market"
        alt=""
      >
    </div>
  </section>
</template>

<script setup>
const explore = () => {
  alert("Mulai Jelajahi Marketplace")
}

const demo = () => {
  alert("Demo Marketplace")
}
</script>

<style scoped>
.hero {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 60px 8%;
  gap: 40px;
  flex-wrap: wrap;
}

.hero-left {
  flex: 1;
}

.hero-left h1 {
  font-size: 3rem;
  color: #164c3b;
  margin: 20px 0;
}

.highlight {
  color: #2c9b7a;
}

.hero-left p {
  color: #3e6b5d;
  margin-bottom: 30px;
}

.hero-right {
  flex: 1;
  text-align: center;
}

.hero-right img {
  width: 100%;
  max-width: 500px;
  border-radius: 30px;
}

.typing-badge {
  display: inline-block;
  background: #daf4ec;
  padding: 6px 14px;
  border-radius: 30px;
}

.cta-group {
  display: flex;
  gap: 20px;
  flex-wrap: wrap;
}

.btn-primary {
  background: #1e6f5c;
  color: white;
  border: none;
  padding: 14px 30px;
  border-radius: 40px;
  cursor: pointer;
}

.btn-outline {
  border: 2px solid #1e6f5c;
  background: transparent;
  padding: 14px 30px;
  border-radius: 40px;
  cursor: pointer;
}

@media(max-width:768px){
  .hero{
    flex-direction: column-reverse;
    text-align: center;
  }

  .hero-left h1{
    font-size: 2rem;
  }

  .cta-group{
    justify-content: center;
  }
}
</style>