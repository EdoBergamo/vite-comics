<script>
export default {
  name: 'AppHeader',
  data() {
    return {
      menu: [
        {
          nome: 'Characters',
          url: '#',
        },
        {
          nome: 'Comics',
          url: '#',
        },
        {
          nome: 'Movies',
          url: '#',
        },
        {
          nome: 'Tv',
          url: '#',
        },
        {
          nome: 'Games',
          url: '#',
        },
        {
          nome: 'Collectibles',
          url: '#',
        },
        {
          nome: 'Videos',
          url: '#',
        },
        {
          nome: 'Fans',
          url: '#',
        },
        {
          nome: 'News',
          url: '#',
        },
        {
          nome: 'Shop',
          url: '#',
        },
        {
          nome: 'Characters',
          url: '#',
        },
        {
          nome: 'Characters',
          url: '#',
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
          <a :href="li.url" target="_blank">
            {{ li.nome }}
          </a>
        </li>
      </ul>

    </div>
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
      }
    }
  }
</style>