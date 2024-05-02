<script setup>

const cardInfo = [
      {
            id: 0, 
            icon: '/images/icon-online.svg',
            title: 'Online Banking',
            description: 'Our modern web and mobile applications allow you to keep track of your finances wherever you are in the world.'
      },
      {
            id: 1, 
            icon: '/images/icon-budgeting.svg',
            title: 'Simple Budgeting',
            description: 'See exactly where your money goes each month. Receive notifications when you’re close to hitting your limits.'
      },
      {
            id: 2, 
            icon: '/images/icon-onboarding.svg',
            title: 'Fast Onboarding',
            description: 'We don’t do branches. Open your account in minutes online and start taking control of your finances right away.'
      },
      {
            id: 3, 
            icon: '/images/icon-api.svg',
            title: 'Open API',
            description: 'Manage your savings, investments, pension, and much more from one account. Tracking your money has never been easier.'
      }
]

</script>

<template>
      <div class="whyChoose ">
            <div class="whyChoose-title">
                  <h2> Why choose Easybank?</h2>
                  <p>
                        We leverage Open Banking to turn your bank account into your financial hub. Control 
                        your finances like never before.
                  </p>
            </div>

            <div class="card-container">
                  <div class="card" v-for="item in cardInfo">
                        <img :src=item.icon alt="" />
                        <h3>{{ item.title }}</h3>
                        <p>{{ item.description }}</p>
                  </div>
            </div>
      </div>

</template>

<style scoped>
.whyChoose {
      display: flex;
      text-align: center;
      flex-direction: column;
      align-items: center;
      background-color: var(--LightGrayishBlue);
      padding: 2rem 0 2rem;
}

.whyChoose-title {
      margin-bottom: 1.5rem;
}

.whyChoose-title h2 {
      font-size: 1.8rem;
      font-weight: 400;
      line-height: 2rem;
      margin-bottom: .8rem;
}

.whyChoose-title p  {
      font-size: .8rem;
      color: var(--GrayishBlue);
      max-width: 20rem;
}

.card {
      margin: 2rem 0;
      max-width: 20rem;
}

.card img {
      margin-bottom: .5rem;
}

.card h3 {
      font-size: 1rem;
      font-weight: 400;
      margin-bottom: .8rem;
}

.card p  {
      font-size: .8rem;
      color: var(--GrayishBlue);
}

@media screen and (min-width: 700px) {
      .whyChoose  {
            padding: 3rem 0 2rem;
            display: flex;
            text-align: left;
            flex-direction: column;
            align-items: start;
      }

      .whyChoose-title h2 {
            font-size: 2.2rem;
            font-weight: 400;
            line-height: 2rem;
            margin-bottom: 1rem;
      }

      .whyChoose-title p  {
            font-size: 1rem;
            max-width: 40rem;
      }

      .card-container {
            width: 100%;
            display: grid;
            grid-template-columns: 1fr 1fr;
            column-gap: 2rem;
      }

      .card {
            max-width: 17rem;
            text-align: center;
      }

      .card h3 {
            font-size: 1.3rem;
      }

      .card p  {
            font-size: .9rem;
      }
}

@media screen and (min-width: 1000px) {
      .whyChoose  {
            padding: 4rem 0 2rem;
            display: flex;
            text-align: left;
            flex-direction: column;
            align-items: start;
      }

      .card-container {
            display: flex;
            justify-content: space-between;
            column-gap: 2rem;
      }

      .card {
            max-width: auto;
            text-align: left;
      }
}
</style>