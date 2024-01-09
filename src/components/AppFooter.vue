<script>
export default {
  name: 'Footer',
  data() {
    return {
      menu: [
        {
          name: 'Dc Comics',
          urls: [
            'Characters',
            'Comics',
            'Movies',
            'TV',
            'Games',
            'Videos',
            'News'
          ],
        },
        {
          name: 'Shop',
          urls: [
            'Shop DC',
            'Shop DC Collectibles'
          ],
        },
        {
          name: 'DC',
          urls: [
            'Terms of Use',
            'Privacy Policy (New)',
            'Ad Choices',
            'Advertising',
            'Jobs',
            'Subscriptions',
            'Talent Workshop',
            'CPSC Certificates',
            'Ratings',
            'Show Help',
            'Contact Us'
          ],
        },
        {
          name: 'Sites',
          urls: [
            'DC',
            'Mad Magazine',
            'DC Kids',
            'DC Universe',
            'DC Power Visa'
          ],
        },
      ]
    }
  }
}
</script>

<template>
  <footer id="footer">
    <div id="top-footer">
      <div class="container">

        <ul class="menu-footer">
          <li v-for="item in menu" class="sections">
            <h2>{{ item.name }}</h2>
            <ul class="labels">
              <li class="label-url" v-for="url in item.urls">
                <a href="#" target="_blank">{{ url }}</a>
              </li>
            </ul>
          </li>
        </ul>

        <img src="../assets/img/dc-logo-bg.png" class="logo" alt="logo">
      </div>
    </div>

    <div id="bottom-footer">
      <div class="container">
        <button class="button-primary">
          Sign-up now!
        </button>


        <div class="right-bottom">
          <h3>Follow Us</h3>
          <div class="social-links">
            <a href="">
              <img class="logo-social" src="../assets/img/footer-facebook.png" alt="">
            </a>
            <a href="">
              <img class="logo-social" src="../assets/img/footer-twitter.png" alt="">
            </a>
            <a href="">
              <img class="logo-social" src="../assets/img/footer-youtube.png" alt="">
            </a>
            <a href="">
              <img class="logo-social" src="../assets/img/footer-pinterest.png" alt="">
            </a>
            <a href="">
              <img class="logo-social" src="../assets/img/footer-periscope.png" alt="">
            </a>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

#top-footer {
  background-image: url('../assets/img/footer-bg.jpg');
  background-size: cover;

  .container {
    max-width: 1300px;
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: space-between;
    overflow: hidden;

    .logo {
      width: 600px;
      max-height: 400px;
      object-fit: cover;
    }
  }
}

.menu-footer {
  display: flex;
  flex-direction: column;
  color: $text-white;
  max-height: 400px;
  padding: 40px 0px 60px;
  gap: 10px 40px;
  flex-wrap: wrap;
  flex-grow: 1;

  align-content: start;

  .labels {
    display: flex;
    flex-direction: column;
    list-style: none;

    .label-url a {
      font-size: 10px;
      padding-top: 8px;
      list-style: none;
      text-decoration: none;
      color: #aba9a9;
    }
  }
}

#bottom-footer {
  background-color: $bottom-footer;

  .container {
    padding: 20px 0;
    display: flex;
    align-items: center;
    max-width: 1300px;
    margin: 0 auto;
    justify-content: space-between;
  }
}

.button-primary {
  padding: 10px 10px;
  border: 2px solid $bg-primary;
  color: $text-white;
  text-transform: uppercase;
  background-color: transparent;
  cursor: pointer;
}

.right-bottom {
  display: flex;
  align-items: center;
  gap: 20px;
  color: $bg-primary;

  .social-links {
    display: flex;
    gap: 15px;

    .logo-social {
      width: 35px;
      display: block;
      padding: 5px;
    }
  }
}
</style>