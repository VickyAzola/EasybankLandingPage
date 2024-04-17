<script setup>
import TheNavbar from './components/TheNavbar.vue';
import TheFooter from './components/TheFooter.vue'
import TheButton from './components/TheButton.vue';
import WhyChoose from './components/WhyChoose.vue'
import Articles from './components/Articles.vue'
import Mockups from '/images/image-mockups.png';
</script>

<template>
  <TheNavbar />
  
  <main class="main-section">
    <section class="hero-section">
      <div class="heroMobile">
        <img :src=Mockups alt="4 Phones showing the mobile App" />
      </div>
      <div class="heroDesktop" >
        <img :src=Mockups alt="4 Phones showing the mobile App" />
      </div>
      <div class="title-section">
        <h1>Next generation <br /> digital banking</h1>
        <p>
          Take your financial life online. Your Easybank account will be a one-stop-shop 
          for spending, saving, budgeting, investing, and much more.
        </p>
        <TheButton text="Request Invite" />
      </div>
    </section>

    <section class="whyChoose-section">
      <WhyChoose />
    </section>

    <section class="articles-section">
      <Articles />
    </section>
  </main>

  <TheFooter />
</template>

<style scoped>
.main-section {
  padding-top: 2rem;
}

.hero-section {
  background-color: var(--VeryLightGray);
}

.heroMobile {
  display: flex;
  justify-content: center;
  background-image: url('/images/bg-intro-mobile.svg');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: top -.6rem right;
}

.heroMobile img {
  width: 20rem;
  margin-top: -4rem;
}

.heroDesktop {
  display: none;
}

.title-section {
  padding: 1rem;
  display: flex;
  text-align: center;
  flex-direction: column;
  row-gap: .6rem;
  align-items: center;
}

.title-section h1 {
  font-size: 2rem;
  font-weight: 400;
  line-height: 2.4rem;
}

.title-section p  {
  font-size: .8rem;
  color: var(--GrayishBlue);
}

.whyChoose-section {
  padding: 1.2rem;
  background-color: var(--LightGrayishBlue);
}

.articles-section {
  padding: 1.5rem;
  background-color: var(--VeryLightGray);
}

@media screen and (min-width: 600px) {
  .heroMobile {
    display: none;
  }

  .hero-section {
    display: grid;
    grid-template-columns: .8fr 1fr;
    column-gap: .5rem;
    overflow: hidden;
    height: 35rem;
  }

  .title-section {
    padding: 0 .5rem 0 3rem;
    margin: auto;
    height: 20rem;
    display: flex;
    row-gap: .7rem;
    text-align: left;
    flex-direction: column;
    align-items: start;
  }

  .title-section h1 {
    font-size: 2rem;
    font-weight: 400;
    line-height: 2.2rem;
  }

  .title-section p  {
    font-size: .8rem;
  }

  .heroDesktop {
    order: 2;
    display: block;
    display: flex;
    justify-content: flex-end;
    background-image: url('/images/bg-intro-desktop.svg');
    background-repeat: no-repeat;
    background-position: top  right -9.5rem;
    background-size: 140%;
    height: 36rem;
  }

  .heroDesktop img {
    position: relative;
    z-index: 2;
    margin-top: -5rem;
    margin-right: -10rem;
    margin-bottom: 5rem;
    width: 30rem;
  }

  .whyChoose-section {
    position: relative;
    z-index: 1;
    margin-top: -9rem;
    padding-inline: 4rem;
  }

  .articles-section {
    padding: 3rem 4rem;
  } 
}

@media screen and (min-width: 1000px) {
  .hero-section {
    grid-template-columns: 1fr 1.3fr;
  }

  .title-section {
    padding: 0 1rem 0 4rem;
    row-gap: .8rem;
  }

  .title-section h1 {
    font-size: 3rem;
    line-height: 3rem;
  }

  .title-section p  {
    font-size: 1rem;
  }

  .heroDesktop {
    background-position: top -5rem right -11rem;
    background-size: 130% 101%;
  }

  .heroDesktop img {
    margin-top: -4rem;
    margin-right: -4rem;
    margin-bottom: 0;
    width: 35rem;
    height: 39rem;
  }

  .whyChoose-section {
    margin-top: -7rem;
  }
}

@media screen and (min-width: 1440px) {
  .hero-section {
    grid-template-columns: 1fr 1.4fr;
    column-gap: 1rem;
  }

  .title-section {
    padding-left: 8rem;
    padding-right: 0;
  }

  .heroDesktop {
    background-position: top -9rem right -10rem;
    background-size: 120% 111%;
  }

  .heroDesktop img {
    margin-top: -2.5rem;
  }

  .whyChoose-section {
    padding-inline: 8rem;
  }

  .articles-section {
    padding-inline: 8rem ;
  } 

}

</style>
