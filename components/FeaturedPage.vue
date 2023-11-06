<template>
    <section class="featured__section" id="featured">

        <span class="featured__title">The Best Product in</span>
        <h2 class="featured__subtitle">F U R N I S H</h2>

        <div class="featured__container" ref="featuredContainer">

            <article class="featured__card" ref="card1">
                <img src="~/assets/img/Chair/Chair.png" class="featured__img" alt="">

                <h3 class="featured__name">PERSEY</h3>

                <span class="featured__description">Grey Sofa With Minimalist Style</span>

                <span class="featured__price">$49</span>

            </article>

            <article class="featured__card" ref="card2">
                <img src="~/assets/img/Chair/Sofa abu.png" class="featured__img img2" alt="">

                <h3 class="featured__name">MULTER</h3>

                <span class="featured__description">Feel Comfortable First</span>

                <span class="featured__price">$79</span>

            </article>

            <article class="featured__card" ref="card3">
                <img src="~/assets/img/Chair/TACCHINI.png" class="featured__img img3" alt="">

                <h3 class="featured__name">TACCHINI</h3>

                <span class="featured__description">Grey Always Inspire Me</span>

                <span class="featured__price">$99</span>

            </article>
        </div>
    </section>
</template>

<script type="module">
export default {
  mounted() {
    this.animateOnScroll();
  },
  methods: {
    animateOnScroll() {
      this.$gsap.registerPlugin(this.$ScrollTrigger);

      // Animasi untuk card 1
      this.$gsap.from(this.$refs.card1, {
        opacity: 0.5,
        y: '-60px',
        duration: 1, // Durasi animasi 1 detik
        delay: 0.2, // Delay 0.5 detik
        scrollTrigger: {
          trigger: this.$refs.featuredContainer,
          start: 'top 100%',
          scrub: true, // Memulai animasi saat 80% dari card masuk ke viewport
        },
      });

      // Animasi untuk card 2 dengan penundaan 4 detik
      this.$gsap.from(this.$refs.card2, {
        opacity: 0.5,
        y: '-60px',
        duration: 1, // Durasi animasi 1 detik
        delay: 0.6, // Delay 4 detik
        scrollTrigger: {
          trigger: this.$refs.featuredContainer,
          start: 'top 100%',
          scrub: true,
        },
      });

      // Animasi untuk card 3 dengan penundaan 4 detik
      this.$gsap.from(this.$refs.card3, {
        opacity: 0.5,
        y: '-60px',
        duration: 1, // Durasi animasi 1 detik
        delay: 1, // Delay 4 detik
        scrollTrigger: {
          trigger: this.$refs.featuredContainer,
          start: 'top 100%',
          scrub: true,
        },
      });
    },
  },
};
</script>








<style>
.featured__section {
    padding-top: 6rem;
    font-family: "Poppins";
    text-align: center;
    height:1000px;
}

.featured__container {
    padding-top: 4rem;
    display: grid;
    grid-template-columns: 250px;
    justify-content: center;
    row-gap: 5.5rem;
    font-family: "Poppins";
}

.featured__subtitle {
    color: rgb(21, 21, 68);
}

.featured__card {
    position: relative;
    background-color: rgb(255, 251, 251);
    padding: 7rem 2rem 1.5rem;
    box-shadow: 0 8px 20px rgba(128, 127, 127, 0.342);
    border-radius: 1rem;
    text-align: center;
    cursor: pointer;
    transition: transform 0.4s;
    /* Menambahkan transisi */
}

.featured__card:hover {
    transform: scale(1.2);
    /* Mengubah ukuran elemen 10% lebih besar saat di-hover */
    z-index: 1;
    /* Mengatur z-index untuk menunjukkan elemen yang di-hover di atas elemen lain */
    box-shadow: 0 16px 32px rgba(128, 127, 127, 0.542);
    /* Shadow yang lebih besar saat di-hover */
}

.featured__img {
    width: 250px;
    position: absolute;
    inset: 0;
    top: -4rem;
    margin: 0 auto;
    transition: transform .4s;
}

.img2 {
    top: -6.5rem;
}

.img3 {
    top: -6rem;
}

.featured__description {
    display: block;
    font-size: .85rem;
    margin-bottom: 1rem;
}

.featured__price {
    color: rgb(21, 21, 68);
    font-size: 1.2rem;
    font-weight: 600;
}

/*=============== BREAKPOINTS ===============*/
/* For small devices */
@media screen and (max-width: 320px) {
    .featured__container {
        padding-top: 4rem;
        display: grid;
        grid-template-columns: 220px;
        justify-content: center;
        row-gap: 5rem;
        font-family: "Poppins";
        margin: 0 1rem;
    }


    .featured__img {
        width: 200px;
        position: absolute;
        inset: 0;
        top: -3rem;
        margin: 0 auto;
        transition: transform .4s;
    }

    .img2 {
        top: -5.5rem;
    }

    .img3 {
        top: -5rem;
    }

    .featured__description {
        display: block;
        font-size: .85rem;
        margin-bottom: 0.85rem;
    }
}

/* For medium devices */
@media screen and (min-width: 576px) {

    .featured__title {
        font-size: 1.5rem;
    }

    .featured__subtitle {
        font-size: 2rem;
        margin-bottom: 1.5rem;
    }
}

/* For medium devices */
@media screen and (min-width: 767px) {
    .featured__container {
        grid-template-columns: repeat(2, 250px);
        column-gap: 1.5rem;
    }
}

@media screen and (min-width: 992px) {
    .featured__container {
        grid-template-columns: repeat(3, 250px);
        column-gap: 2.5rem;
    }
}

@media screen and (min-width: 1024px) {
    .featured__container {
        grid-template-columns: repeat(3, 350px);
        column-gap: 2.5rem;
    }

    .featured__card {
        margin-top: 3rem;
    }

    .featured__img {
        width: 270px;
        position: absolute;
        inset: 0;
        top: -4.5rem;
        margin: 0 auto;
        transition: transform .4s;
    }

    .img2 {
        top: -7rem;
    }

    .img3 {
        top: -6rem;
    }
}</style>