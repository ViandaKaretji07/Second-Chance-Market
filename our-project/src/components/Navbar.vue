<template>
  <div class="navbar">
    <div class="logo">
      <i class="fas fa-leaf"></i>
      Second Chance Market
    </div>

    <div class="nav-links">
      <a href="#">Beranda</a>
      <a href="#fitur">Fitur</a>
      <a href="#cara-kerja">Panduan</a>

      <a href="#" class="btn-masuk" @click.prevent="goToMarket">
        <i class="fas fa-store"></i>
        Masuk Marketplace
      </a>
    </div>
  </div>
</template>

<script setup>
const goToMarket = () => {
  alert("Menuju Marketplace")
}
</script>

<style scoped>
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 8%;
  background: rgba(255,255,255,0.95);
  position: sticky;
  top: 0;
  z-index: 100;
  backdrop-filter: blur(10px);
}

.logo {
  font-size: 1.8rem;
  font-weight: 800;
  color: #1e6f5c;
}

.logo i {
  margin-right: 8px;
  color: #3ca17e;
}

.nav-links {
  display: flex;
  align-items: center;
  gap: 14px;
}

.nav-links a {
  text-decoration: none;
  color: #2c5e4c;
  font-weight: 600;
}

.btn-masuk {
  background: #1e6f5c;
  color: white !important;
  padding: 10px 24px;
  border-radius: 40px;
}

@media(max-width:768px){
  .navbar{
    flex-direction: column;
  }
}
</style>