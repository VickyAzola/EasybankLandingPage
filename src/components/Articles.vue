<script setup>

const articleInfo = [
    {
        id: 0, 
        img: '/images/image-currency.jpg',
        alt: 'Money',
        autor: 'By Claire Robinson',
        title: 'Receive money in any currency with no fees',
        description: 'The world is getting smaller and we’re becoming more mobile. So why should you be forced to only receive money in a single …'
    },
    {
        id: 1, 
        img: '/images/image-restaurant.jpg',
        alt: 'People eating at a restaurant',
        autor: 'By Wilson Hutton',
        title: 'Treat yourself without worrying about money',
        description: 'Our simple budgeting feature allows you to separate out your spending and set realistic limits each month. That means you …'
    },
    {
        id: 2, 
        img: '/images/image-plane.jpg',
        alt: 'A plane flying in the sky',
        autor: 'By Wilson Hutton',
        title: 'Take your Easybank card wherever you go',
        description: 'We want you to enjoy your travels. This is why we don’t charge any fees on purchases while you’re abroad. We’ll even show you …'
    },
    {
        id: 3, 
        img: '/images/image-confetti.jpg',
        alt: 'confetti',
        autor: 'By Claire Robinson',
        title: 'Our invite-only Beta accounts are now live!',
        description: 'After a lot of hard work by the whole team, we’re excited to launch our closed beta. It’s easy to request an invite through the site ...'
    }
]

</script>


<template>
    <div>
        <div class="articles-title">
            <h4>Latest Articles</h4>
        </div>

        <div class="article-container">
            <article class="card-article" v-for="item in articleInfo">
                <img :src=item.img :alt=item.alt />
                <div class="text">
                    <p class="autor">{{ item.autor }}</p>
                    <h5>{{ item.title }}</h5>
                    <p class="description">{{ item.description }}</p>
                </div>
            </article>
        </div>
    </div>
</template>

<style scoped>

.articles-title h4 {
    padding: 2rem 0 1rem;
    font-size: 1.8rem;
    font-weight: 400;
    text-align: center;
}

.card-article {
    margin-bottom: 3rem;
    background-color: white;
}

.card-article img {
    border-radius: .5rem .5rem 0 0;
    height: 12rem;
    width: 100%;
}

.card-article .text {
    padding: 1rem;
}

.card-article .autor {
    margin-bottom: .5rem;
    color: var(--GrayishBlue);
    font-size: .8rem;
}

.card-article h5 {
    font-size: 1rem;
    font-weight: 400;
    margin-bottom: .8rem;
}

.card-article h5:hover {
    color: var(--LimeGreen);
    cursor: pointer;
}

.card-article .description  {
    font-size: .8rem;
    color: var(--GrayishBlue);
}

@media screen and (min-width: 600px) {

.card-article {
    margin-bottom: 2rem;
    max-width: 17rem;
}

.articles-title h4 {
    font-size: 2.5rem;
    margin-bottom: 1.5rem;
    text-align: left;
}

.article-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    column-gap: 1rem;
}
}

@media screen and (min-width: 1000px) {

    .article-container {
        flex-wrap: nowrap;
        column-gap: 1.2rem;
    }

    .card-article {
        max-width: auto;
    }
}

</style>