<template>
  <section class="testimoni">
    <div class="section-title">
      Apa Kata Mereka?
    </div>

    <div class="testimonial-wrapper">
      <button class="nav-btn left" @click="prevTestimonial">
        <i class="fas fa-chevron-left"></i>
      </button>

      <div class="testimonial-container">
        <div
          v-for="(item, index) in visibleTestimonials"
          :key="item.id"
          class="testi-card"
          :class="{
            active: index === 1,
            side: index !== 1
          }"
        >
          <div class="stars">
            <i
              v-for="star in 5"
              :key="star"
              class="fas fa-star"
            ></i>
          </div>

          <p class="testimonial-text">
            "{{ item.text }}"
          </p>

          <h4>
            — {{ item.name }}, {{ item.major }}
          </h4>
        </div>
      </div>

      <button class="nav-btn right" @click="nextTestimonial">
        <i class="fas fa-chevron-right"></i>
      </button>
    </div>

    <div class="indicator">
      <span
        v-for="(item, index) in testimonials"
        :key="item.id"
        :class="{ active: currentIndex === index }"
      ></span>
    </div>

    <div class="cta-wrapper">
      <button class="btn-primary-landing" @click="goToMarket">
        <img
          src="@/assets/image/logo.png"
          alt="Logo"
          class="btn-logo"
        />
        <span>Coba Sekarang</span>
      </button>
    </div>
  </section>
</template>

<script>
export default {
  name: "Testimoni",

  data() {
    return {
      currentIndex: 0,

      testimonials: [
        {
          id: 1,
          name: "Dina",
          major: "Informatika 2022",
          text: "Aku bisa menjual lemari bekas sebelum pulang kampung. Fitur titip jual sangat membantu dan dalam dua hari barangku langsung laku."
        },
        {
          id: 2,
          name: "Rizky",
          major: "Sistem Informasi 2021",
          text: "Second Chance Market membuatku lebih mudah menjual barang yang sudah tidak terpakai tanpa harus mencari pembeli sendiri."
        },
        {
          id: 3,
          name: "Sarah",
          major: "Teknik Industri 2023",
          text: "Aku mendapatkan meja belajar dengan harga yang jauh lebih murah. Kondisinya masih bagus dan sesuai dengan deskripsi."
        },
        {
          id: 4,
          name: "Andi",
          major: "Teknik Informatika 2022",
          text: "Fitur chat sangat memudahkan proses negosiasi. Semuanya terasa lebih praktis karena dilakukan dalam satu platform."
        },
        {
          id: 5,
          name: "Nabila",
          major: "Manajemen 2021",
          text: "Platform ini membantu mahasiswa menghemat pengeluaran sekaligus mengurangi barang bekas yang tidak terpakai."
        }
      ]
    };
  },

  computed: {
    visibleTestimonials() {
      const total = this.testimonials.length;

      const prevIndex =
        (this.currentIndex - 1 + total) % total;

      const nextIndex =
        (this.currentIndex + 1) % total;

      return [
        this.testimonials[prevIndex],
        this.testimonials[this.currentIndex],
        this.testimonials[nextIndex]
      ];
    }
  },

  methods: {
    nextTestimonial() {
      this.currentIndex =
        (this.currentIndex + 1) %
        this.testimonials.length;
    },

    prevTestimonial() {
      this.currentIndex =
        (this.currentIndex - 1 + this.testimonials.length) %
        this.testimonials.length;
    },

    goToMarket() {
      alert(
        "✨ Menuju ke Marketplace Second Chance Market ✨\n(Dalam implementasi nyata, ini akan membuka halaman marketplace.)"
      );

      window.open("#", "_self");
    }
  },

  mounted() {
    const observer = new IntersectionObserver(
      (entries) => {
        entries.forEach((entry) => {
          if (entry.isIntersecting) {
            entry.target.classList.add("show");
          }
        });
      },
      {
        threshold: 0.2
      }
    );

    const section = document.querySelector(".testimonial-wrapper");

    if (section) {
      observer.observe(section);
    }
  }
};
</script>