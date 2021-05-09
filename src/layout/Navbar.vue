<template>
  <div id="navbar">
    <div class="logo">
      <img src="../assets/img/logo.svg" alt="" />
    </div>
    <div class="links-div">
      <ul>
        <li class="link">
          <a
            href="#"
            @click="getActive('home')"
            :class="{ active: active == 'home' }"
            >home</a
          >
        </li>
        <li class="link">
          <a
            href="#"
            @click="getActive('about')"
            :class="{ active: active == 'about' }"
            >about</a
          >
        </li>
        <li class="link">
          <a
            href="#"
            @click="getActive('contact')"
            :class="{ active: active == 'contact' }"
            >contact</a
          >
        </li>
        <li class="link">
          <a
            href="#"
            @click="getActive('blog')"
            :class="{ active: active == 'blog' }"
            >blog</a
          >
        </li>
        <li class="link">
          <a
            href="#"
            @click="getActive('careers')"
            :class="{ active: active == 'careers' }"
            >careers</a
          >
        </li>
      </ul>
    </div>
    <div class="request-btn">
      <RequestButton />
    </div>
    <v-dialog v-model="dialog">
      <template v-slot:activator="{ on, attrs }">
        <div class="dialog-button">
          <v-btn class="dialog-button mt-3" v-bind="attrs" v-on="on" text width="0" height="0">
          <img src="../assets/img/icon-close.svg" alt="" v-if="dialog" />
          <img src="../assets/img/icon-hamburger.svg" alt="" v-if="!dialog" />
        </v-btn>
        </div>
      </template>

      <v-card>
        <v-card-text>
          <ul>
            <li class="link link-1">
              <a href="#">Home</a>
            </li>
            <li class="link link-2">
              <a href="#">About</a>
            </li>
            <li class="link link-3">
              <a href="#">Contact</a>
            </li>
            <li class="link link-4">
              <a href="#">Blog</a>
            </li>
            <li class="link">
              <a href="#">Careers</a>
            </li>
          </ul>
        </v-card-text>
      </v-card>
    </v-dialog>
  </div>
</template>

<script>
import RequestButton from "../components/RequestButton";

export default {
  components: {
    RequestButton,
  },
  data() {
    return {
      active: "home",
      dialog: false,
    };
  },
  methods: {
    getActive(val) {
      this.active = val;
    },
    hamburgerChange() {
      this.hamburger = !this.hamburger;
    },
  },
};
</script>

<style lang="scss">
.v-dialog {
  position: absolute;
  top: 4rem;
  width: 90vw !important;

  .v-card {
    padding: 3rem 0rem;
    ul {
      padding: 0;
      list-style: none;
      text-align: center;
    }

    a {
      color: hsl(233, 26%, 24%);
      font-weight: 400;
      font-size: 2rem;
      text-transform: capitalize;
      text-decoration: none;
      display: inline-block;

      &:hover {
        color: hsl(136, 65%, 51%);
        font-weight: 700;
      }
    }

    .link-1, .link-2, .link-3, .link-4 {
      margin-bottom: 4rem;
    }
  }
}
#navbar {
  display: flex;
  justify-content: space-between;
  padding: 1.3rem 15rem;
  border-bottom: 0.1px solid #fff;
  box-shadow: 0rem 0.3rem 1rem hsl(233, 8%, 62%);
  position: relative;
  background-color: #fff;
  z-index: 999999;
  // height: 5.1rem;

  .dialog-button {
    display: none !important;
  }

  .hamburger {
    display: none;
  }

  .links-div {
    ul {
      padding: 0;
      list-style: none;
      display: table;
      width: 40rem;
      text-align: center;
    }
    li {
      display: table-cell;
      position: relative;
    }

    a {
      color: hsl(233, 8%, 62%);
      font-weight: 700;
      font-size: 1.3rem;
      text-transform: capitalize;
      text-decoration: none;

      display: inline-block;
      padding: 0rem 0.5rem;
      position: relative;

      &:hover {
        color: hsl(233, 26%, 24%);
      }
    }
    a:after {
      background: none repeat scroll 0 0 transparent;
      bottom: -2.5rem;
      content: "";
      display: block;
      height: 0.4rem;
      left: 50%;
      position: absolute;
      background: hsl(136, 65%, 51%);
      transition: width 0.3s ease 0s, left 0.3s ease 0s;
      width: 0;
    }
    a:hover:after,
    a.active:after {
      width: 100%;
      left: 0;
    }
  }
}
</style>