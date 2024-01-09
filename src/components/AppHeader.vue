<script>
import AppJumbotron from './AppJumbotron.vue'
export default {
  name: 'AppHeader',
  components: {
    AppJumbotron
  },
  data() {
    return {
      menu: [
        {
          nome: 'Characters',
          url: '#',
          active: false
        },
        {
          nome: 'Comics',
          url: '#',
          active: true
        },
        {
          nome: 'Movies',
          url: '#',
          active: false
        },
        {
          nome: 'Tv',
          url: '#',
          active: false
        },
        {
          nome: 'Games',
          url: '#',
          active: false
        },
        {
          nome: 'Collectibles',
          url: '#',
          active: false
        },
        {
          nome: 'Videos',
          url: '#',
          active: false
        },
        {
          nome: 'Fans',
          url: '#',
          active: false
        },
        {
          nome: 'News',
          url: '#',
          active: false
        },
        {
          nome: 'Shop',
          url: '#',
          active: false
        },
        {
          nome: 'Characters',
          url: '#',
          active: false
        },
        {
          nome: 'Characters',
          url: '#',
          active: false
        },
      ]
    }
  }
}
</script>

<template>
  <header>
    <div id="navbar">

      <div class="logo">
        <img src="../assets/img/dc-logo.png" alt="Logo" />
      </div>

      <ul class="list-links">
        <li class="link" v-for="li in menu">
          <a :href="li.url" :class="li.active ? 'active' : ''" target="_blank">
            {{ li.nome }}
          </a>
        </li>
      </ul>

    </div>
    <AppJumbotron />
  </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

#navbar {
  justify-content: space-between;
  height: 120px;
  display: flex;
  align-items: center;
  max-width: 1300px;
  margin: 0 auto;
}

.logo {
  width: 80px;

  img {
    width: 100%;
    display: block;
  }
}

.list-links {
  display: flex;
  gap: 35px;

  .link {
    list-style: none;
    line-height: 120px;
    border-bottom: 2px solid transparent;

    &:hover {
      color: $bg-primary;
      border-bottom: 2px solid $bg-primary;
    }

    a {
      all: unset;
      font-weight: 600;
      text-decoration: none;

      &.active {
        color: $bg-primary;
        border-bottom: 2px solid $bg-primary;
      }
    }
  }
}
</style>