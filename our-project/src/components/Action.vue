<template>
  <div class="aida-action-section">
    <i class="fas fa-bullhorn" style="font-size: 2.5rem; margin-bottom: 10px;"></i>
    <h3>🚀 Mulai sekarang, jangan biarkan barang bekasmu berdebu di sudut kamar.</h3>
    <p>
      Upload produkmu di <strong>Second Chance Market</strong> dan temukan pembeli yang tepat.<br>
      <i class="fas fa-mouse-pointer"></i> Klik, jual, dan wujudkan peluang baru dari barang lama.
    </p>
    <button @click="handleAction" class="btn-action-large">
      <i class="fas fa-hand-peace"></i> {{ buttonText }}
    </button>
  </div>
</template>

<script>
export default {
  name: 'CallToAction',
  props: {
    buttonText: {
      type: String,
      default: 'Jual Sekarang & Raih Peluang Baru'
    }
  },
  methods: {
    handleAction() {
      // Emit event ke parent component
      this.$emit('action-click');
      
      // Bisa juga langsung panggil method atau router
      // this.$router.push('/marketplace');
    }
  }
}
</script>

<style scoped>
.aida-action-section {
  background: linear-gradient(135deg, #1e6f5c, #0f5444);
  border-radius: 48px;
  margin: 0 8% 50px 8%;
  padding: 40px 30px;
  text-align: center;
  color: white;
  box-shadow: 0 20px 35px rgba(0,0,0,0.1);
  transition: transform 0.3s ease;
}

.aida-action-section:hover {
  transform: translateY(-5px);
}

.aida-action-section h3 {
  font-size: 1.8rem;
  margin-bottom: 15px;
}

.aida-action-section p {
  font-size: 1.1rem;
  margin-bottom: 25px;
  opacity: 0.95;
}

.btn-action-large {
  background: #ffd966;
  color: #1e6f5c;
  border: none;
  padding: 14px 42px;
  border-radius: 60px;
  font-weight: bold;
  font-size: 1.1rem;
  cursor: pointer;
  transition: all 0.3s ease;
  box-shadow: 0 6px 14px rgba(0,0,0,0.2);
}

.btn-action-large:hover {
  background: #ffcd38;
  transform: scale(1.05);
  box-shadow: 0 10px 20px rgba(0,0,0,0.25);
}

@media (max-width: 768px) {
  .aida-action-section {
    margin: 0 5% 40px 5%;
    padding: 30px 20px;
  }
  
  .aida-action-section h3 {
    font-size: 1.4rem;
  }
  
  .btn-action-large {
    padding: 12px 28px;
    font-size: 1rem;
    width: 100%;
  }
}
</style>