<template>
  <section class="features" id="fitur">
    <h2 class="section-title">
      Fitur Andalan untuk Mahasiswa
    </h2>

    <div class="feature-grid">
      <div
        class="feature-card"
        v-for="feature in features"
        :key="feature.title"
      >
        <div class="feature-icon">
          <i :class="feature.icon"></i>
        </div>

        <h3>{{ feature.title }}</h3>
        <p>{{ feature.desc }}</p>
      </div>
    </div>
  </section>
</template>

<script setup>
const features = [
  {
    icon: 'fas fa-box-open',
    title: 'Post Barang',
    desc: 'Upload barang dengan mudah'
  },
  {
    icon: 'fas fa-comment-dots',
    title: 'Chat Realtime',
    desc: 'Komunikasi penjual dan pembeli'
  },
  {
    icon: 'fas fa-heart',
    title: 'Wishlist',
    desc: 'Simpan barang favorit'
  },
  {
    icon: 'fas fa-plane-departure',
    title: 'Titip Jual',
    desc: 'Jual barang saat mudik'
  }
]
</script>

<style scoped>
.features {
  background: white;
  padding: 60px 8%;
  border-radius: 50px 50px 0 0;
}

.section-title {
  text-align: center;
  margin-bottom: 40px;
  color: #164c3b;
}

.feature-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit,minmax(250px,1fr));
  gap: 30px;
}

.feature-card {
  background: #f9fffc;
  padding: 30px;
  border-radius: 30px;
  text-align: center;
  transition: 0.3s;
}

.feature-card:hover {
  transform: translateY(-10px);
}

.feature-icon {
  font-size: 3rem;
  color: #1e6f5c;
  margin-bottom: 20px;
}
</style>