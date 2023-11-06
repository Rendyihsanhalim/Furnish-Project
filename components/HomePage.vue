<template>
      <section class="home">
        <div class="home__container">
          <img
        ref="homeImg"
        src="~/assets/img/Sofa/SOFAHOME.png"
        class="home__img"
        alt=""
      />


            <div class="home__text" ref="homeText">
              <h1 class="home__title">The Creative<br>Space Edition.</h1>

              <p class="home__description">Minimalist as you can and see your future furniture here </p>

              <a class="button__home button_flex">
                Explore <i class="fa-solid fa-arrow-right button__icon"></i>
              </a>

            </div>
            <div  ref="homeSocial" class="home__social">
              <span class="social__follow">Follow Us</span>
              <div class="social__menu">
                  <a href="" class="social__link"><i class="fa-brands fa-instagram"></i></a>
                  <a href="" class="social__link"><i class="fa-brands fa-github"></i></a>
                  <a href="" class="social__link"><i class="fa-brands fa-linkedin"></i></a>
              </div>
            </div>
          </div>
      </section>
</template>


<script>
import gsap from 'gsap';

export default {
  mounted() {
    const homeImg = this.$refs.homeImg;
    const homeText = this.$refs.homeText;
    const homeSocial = this.$refs.homeSocial;

    gsap.from(homeImg, {
      opacity: 0,
      y: '-60px',  // Menggunakan '60px' untuk jarak
      duration: 2.5,  // Durasi animasi (2.5 detik)
      delay: 0.65,  // Delay sebelum animasi dimulai (0.4 detik)
    });

    
    gsap.from(homeSocial, {
      opacity: 0,
      y: '-60px',  // Menggunakan '60px' untuk jarak
      duration: 2.5,  // Durasi animasi (2.5 detik)
      delay: 0.85,  // Delay sebelum animasi dimulai (0.4 detik)
    });

    gsap.from(homeText, {
      opacity: 0,
      y: '-60px',  // Menggunakan '60px' untuk jarak
      duration: 2.5,  // Durasi animasi (2.5 detik)
      delay: 0.4,  // Delay sebelum animasi dimulai (0.4 detik)
    });
  },
};
</script>

  
  <style scoped>

  .home{
    margin-inline: 2rem;
    padding-top:4rem;
  }

  .home__container{
    display:grid;
    grid-template-rows: repeat(2,max-content);
    row-gap: 2rem;
    position:relative;
  }

  .home__img{
    width:300px;
    filter: drop-shadow(5px 5px 10px rgb(209, 209, 209));
    justify-self: center;
  }

  .home__text{
    font-family: "Poppins";
  }

  .home__title{
    font-size: 2.5rem;
    color:rgb(0, 0, 0);
    font-weight: 600;
    margin-bottom: 1rem;
    line-height: 4rem;
  }

  .home__description{
    font-size:1.25rem;
    margin-bottom: 3rem;
    line-height:1.75rem;
  }

  .button__home{
    display:inline-block;
    background-color:rgb(29, 29, 49);
    color:white;
    padding:1rem 1.75rem;
    border-radius: .5rem;
    font-weight: 400;
    transition:.3s;
    cursor: pointer;

  }

  .button__home:hover{
    background-color: rgb(21, 21, 68)
  }

  .button__icon{
    transition:.3s;
  }

  .button__home:hover .button__icon{
    transform:translateX(.5rem);
  }

  .button_flex{
    display:inline-flex;
    align-items:center;
    column-gap:.5rem;
  }

  .home__social{
    position:absolute;
    top:3.5rem;
    right:-2rem;
    display:grid;
    justify-items: center;
    row-gap :3.5rem;
  }
  .social__follow{
    font-weight: 400;
    font-size: 1rem;
    color:rgb(21, 21, 68);
    transform: rotate(90deg);
    font-family: "Poppins";
    position:relative;
  }

  .social__link{
    color:black;
    font-size: 1rem;
  }
  .social__menu{
    display:inline-flex;
    flex-direction: column;
    row-gap:.25rem;
    justify-content: center;
    align-items: center;
    justify-self: center;
  }

/*=============== BREAKPOINTS ===============*/
/* For small devices */

    @media screen and (max-width: 320px)  {

      .home__container{
        row-gap: 3rem;
      }
      .home__title{

        font-size:1.5rem;
        line-height:3rem;

      }

      .home__description{
        font-size:1rem;
      }

      .home__img{
        width:200px;
      }

    }

      /* For Medium devices */
    @media screen and (min-width: 576px) {
      .home__img{
        width:450px;
      }

      .home__social{
        right:-2rem;
      }

      .social__follow{
  
    font-size: 1.25rem;
   
  }

  .social__link{
    color:black;
    font-size: 1.25rem;
  }
    }

  /* For large devices */
  @media screen and (min-width: 992px) {

    .home{
    padding:8rem 0 0 2rem;
  }

    .home__container{
    display:grid;
    grid-template-columns: repeat(2,max-content);
    column-gap: 2rem;
    position:relative;
  
    }

    .home__img{
      width:350px;
      order:1;
    }
    .home__text{
      width:450px;
    }

    .home__title{

    font-size:3.5rem; 
    line-height:5rem;


  }

  @media screen and (min-width: 1024px) {
    .home__img{
      width:550px;
      order:1;
    }

    .home__container{
      align-items: center;
      column-gap: 3rem;
    }
  }

}
  </style>
  