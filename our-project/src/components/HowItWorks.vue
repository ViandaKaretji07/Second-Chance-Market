<template>
  <section class="how-it-works" id="cara-kerja">
    <h2 class="section-title">
      Cara Kerja Second Chance Market
    </h2>

    <div class="steps">
      <div class="step" v-for="step in steps" :key="step.number">
        <div class="step-number">
          {{ step.number }}
        </div>

        <h3>{{ step.title }}</h3>
        <p>{{ step.desc }}</p>
      </div>
    </div>
  </section>
</template>

<script setup>
const steps = [
  {
    number: 1,
    title: 'Posting Barang',
    desc: 'Upload barang bekasmu'
  },
  {
    number: 2,
    title: 'Negosiasi',
    desc: 'Chat dan tawar harga'
  },
  {
    number: 3,
    title: 'Transaksi',
    desc: 'Lakukan transaksi aman'
  },
  {
    number: 4,
    title: 'Rating',
    desc: 'Beri ulasan pembeli'
  }
]
</script>

<style scoped>
.how-it-works {
  padding: 60px 8%;
  background: #eef5f2;
}

.section-title {
  text-align: center;
  margin-bottom: 40px;
}

.steps {
  display: flex;
  gap: 30px;
  flex-wrap: wrap;
  justify-content: center;
}

.step {
  text-align: center;
  max-width: 250px;
}

.step-number {
  width: 60px;
  height: 60px;
  background: #1e6f5c;
  color: white;
  border-radius: 50%;
  margin: auto;
  display: flex;
  justify-content: center;
  align-items: center;
  font-weight: bold;
  margin-bottom: 20px;
}
</style>