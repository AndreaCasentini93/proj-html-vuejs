<template>
  <div id="app">
    <!-- HEADER -->
    <Header :links="menuLinks" :socials="manuSocials"/>
    <!-- /HEADER -->

    <!-- MAIN -->
    <Main @userEmail="enterEmail"/>
    <!-- /MAIN -->

    <!-- FOOTER -->
    <Footer :socials="manuSocials" :contacts="contactsMaxCoach" :explore="exploreLinks" :information="informationLinks"/>
    <!-- /FOOTER -->

    <!-- FIXED -->
    <div id="fixed_options" class="position-fixed">
      <ul>
        <li>
          <a href="#">
            <i class="fas fa-ruler-combined"></i>
          </a>
        </li>
        <li>
          <a href="#">
            <i class="far fa-life-ring"></i>
          </a>
        </li>
        <li>
          <a href="#">
            <i class="fas fa-book"></i>
          </a>
        </li>
        <li>
          <a href="#">
            <i class="fas fa-shopping-cart"></i>
          </a>
        </li>
      </ul>
    </div>
    <a href="#" id="fixed_arrow" class="position-fixed">&uarr;</a>
    <!-- /FIXED -->
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
          url: '#',
          dropdowns: true
        },
        {
          text: 'Pages',
          url: '#',
          dropdowns: true
        },
        {
          text: 'Courses',
          url: '#',
          dropdowns: true
        },
        {
          text: 'Features',
          url: '#',
          dropdowns: true
        },
        {
          text: 'Blog',
          url: '#',
          dropdowns: true
        },
        {
          text: 'Shop',
          url: '#',
          dropdowns: true
        }
      ],
      manuSocials: [
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
      contactsMaxCoach: {
        address: '382 NE 191st ST # 8739 Miami, FL 33179-3899',
        phone: '+1(305) 547-9909 (9am - 5pm Est, Monday - Friday)',
        email: 'support@maxcoach.com'
      },
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
      userEmail: ''
    }
  },
  methods: {
    enterEmail: function(val) {
      this.userEmail = val;
      console.log(this.userEmail);
    }
  }
}
</script>

<style lang="scss">
  @import './assets/style/general.scss';

  #fixed_options {
    top: 50px;
    right: 0;
    padding: 0 10px;
    border-radius: 10px 0 0 10px;
    font-size: 14px;
    background-color: #FFFFFF;
    box-shadow: 0 0 10px 1px lighten($base-color, 30%);
    z-index: 3;
    
    ul {
      li {
        margin: 10px 0;

        a {
          color: $link-color;
          @include transition-type-1(color);

          &:hover {
            color: lighten($link-color, 40%);
          }
        }
      }
    }
  }
  #fixed_arrow {
    right: 20px;
    bottom: 20px;
    width: 40px;
    line-height: 20px;
    padding: 10px;
    border-radius: 50%;
    text-align: center;
    font-size: 23px;
    font-weight: 700;
    color: #FFFFFF;
    background-color: $ashtag-color;
    @include transition-type-1(background-color);
    z-index: 3;

    &:hover {
      background-color: lighten($ashtag-color, 20%);
    }
  }
</style>
