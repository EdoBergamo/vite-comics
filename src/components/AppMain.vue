<script>
import Card from './Card.vue'

export default {
  name: 'Main',
  components: {
    Card
  },
  data() {
    return {
      data: '',
      goals: [
        {
          name: 'Digital comics',
          path: '../../src/assets/img/buy-comics-digital-comics.png',
          alt: ''
        },
        {
          name: 'Dc merchandise',
          path: '../../src/assets/img/buy-comics-merchandise.png',
          alt: ''
        },
        {
          name: 'Subscription',
          path: '../../src/assets/img/buy-comics-subscriptions.png',
          alt: ''
        },
        {
          name: 'Comics shop locator',
          path: '../../src/assets/img/buy-comics-shop-locator.png',
          alt: ''
        },
        {
          name: 'Dc power visa',
          path: '../../src/assets/img/buy-dc-power-visa.svg',
          alt: ''
        },
      ],
      cards: [
        {
          "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
          "price": "$19.99",
          "series": "Action Comics",
          "type": "comic book",
        },
        {
          "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
          "price": "$3.99",
          "series": "American Vampire 1976",
          "type": "comic book",
        },
        {
          "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
          "price": "$16.99",
          "series": "Aquaman",
          "type": "graphic novel",
        },
        {
          "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
          "price": "$2.99",
          "series": "Batgirl",
          "type": "comic book",
        },
        {
          "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
          "price": "$3.99",
          "series": "Batman",
          "type": "comic book",
        },
        {
          "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
          "price": "$2.99",
          "series": "Batman Beyond",
          "type": "comic book",
        },
        {
          "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
          "price": "$3.99",
          "series": "Batman/Superman",
          "type": "comic book",
        },
        {
          "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
          "price": "$4.99",
          "series": "Batman/Superman Annual",
          "type": "comic book",
        },
        {
          "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
          "price": "$5.99",
          "series": "Batman: The Joker War Zone",
          "type": "comic book",
        },
        {
          "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
          "price": "$6.99",
          "series": "Batman: Three Jokers",
          "type": "comic book",
        },
        {
          "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
          "price": "$4.99",
          "series": "Batman: White Knight Presents: Harley Quinn",
          "type": "comic book",
        },
        {
          "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
          "price": "$16.99",
          "series": "Catwoman",
          "type": "graphic novel",
        },
      ]
    }
  }
}
</script>

<template>
  <main>
    <section id="top-main">
      <div class="container">
        <h2 class="section-title">Current Series</h2>

        <div class="container-2">
          <ul class="cards-list">
            <Card v-for="card in cards" :image="card.thumb" :title="card.series" />
          </ul>
          <button class="fill-button">
            <h4>Load More</h4>
          </button>
        </div>
      </div>
    </section>

    <div id="bottom-main">
      <div class="container-goal">
        <ul class="goals">
          <li class="goal" v-for="item in goals">
            <img :src="item.path" :alt="item.alt" />
            <h3>{{ item.name }}</h3>
          </li>
        </ul>
      </div>
    </div>
  </main>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

#top-main {
  background-color: $background;

  .container {
    max-width: 1300px;
    margin: 0 auto;
    position: relative;

    .section-title {
      background-color: $bg-primary;
      color: $text-white;
      padding: 10px 20px;
      display: inline-block;
      position: absolute;
      top: -25px;
    }

    .container-2 {
      max-width: 1180px;
      margin: 0 auto;
      text-align: center;
      padding: 0 0 20px;

      .cards-list {
        display: flex;
        flex-wrap: wrap;
        gap: 50px 20px;
        padding: 50px 0;
        color: $text-white;

        .card {
          width: calc((100% - 100px) / 6);
        }
      }
    }
  }
}

.fill-button {
  all: unset;
  background-color: $bg-primary;
  padding: 10px 50px;
  color: $text-white;
  text-transform: uppercase;
}

#bottom-main {
  background-color: $bg-primary;
  color: $text-white;

  .container-goal {
    max-width: 1300px;
    margin: 0 auto;
    padding: 50px 0;

    .goals {
      display: flex;
      align-items: center;
      gap: 30px;

      .goal {
        display: flex;
        align-items: center;
        text-transform: uppercase;
        justify-content: center;
        gap: 15px;

        img {
          width: 50px;
        }
      }
    }
  }
}
</style>