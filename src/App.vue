<template>
  <div id="app">
    <!-- HEADER -->
    <Header />
    <!-- /HEADER -->

    <!-- MAIN -->
    <Main />
    <!-- /MAIN -->

    <!-- FOOTER -->
    <Footer />
    <!-- /FOOTER -->
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer
  },
  data:function() {
    return {
      menuLinks: [
        {
          text: 'Home',
          url: '#'
        },
        {
          text: 'Pages',
          url: '#'
        },
        {
          text: 'Courses',
          url: '#'
        },
        {
          text: 'Features',
          url: '#'
        },
        {
          text: 'Blog',
          url: '#'
        },
        {
          text: 'Shop',
          url: '#'
        }
      ],
      manuSocials1: [
        {
          class: 'fab fa-twitter',
          url: '#'
        },
        {
          class: 'fab fa-facebook-f',
          url: '#'
        },
        {
          class: 'fab fa-instagram',
          url: '#'
        },
        {
          class: 'fab fa-linkedin',
          url: '#'
        }
      ],
      exploreLinks: [
        {
          text: 'Start here',
          url: '#'
        },
        {
          text: 'Success stor',
          url: '#'
        },
        {
          text: 'Blog',
          url: '#'
        },
        {
          text: 'Courses',
          url: '#'
        },
        {
          text: 'Contact us',
          url: '#'
        }
      ],
      informationLinks: [
        {
          text: 'Membership',
          url: '#'
        },
        {
          text: 'Purchase guide',
          url: '#'
        },
        {
          text: 'Privacy policy',
          url: '#'
        },
        {
          text: 'Terms of services',
          url: '#'
        }
      ],
    }
  }
}
</script>

<style lang="scss">
  @import './assets/style/general.scss';
</style>
