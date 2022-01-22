<template>
  <div>
    <div class="container">
      <div class="navigation">
        <div class="logo">Sarunas Lekstutis</div>
        <ul class="navigation__links" :class="{ nav__menu: activeNavbar }">
          <li @click="scroll('home')">home</li>
          <li @click="scroll('services')">services</li>
          <li @click="scroll('projects')">projects</li>
          <li @click="scroll('about')">about</li>
          <li @click="scroll('contact')" class="navigation__links-action">
            contact me
          </li>
        </ul>
        <div class="call-action" @click="scroll('contact')">
          <ContactBtn>contact me</ContactBtn>
        </div>
        <div
          class="navigation__menu"
          v-if="!activeNavbar"
          @click="activeNavbar = true"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="26"
            height="16"
            viewBox="0 0 26 16"
          >
            <g transform="translate(-335.5 -23.5)">
              <line
                x2="24"
                transform="translate(336.5 24.5)"
                fill="none"
                stroke="#fff"
                stroke-linecap="round"
                stroke-width="2"
              />
              <line
                x2="24"
                transform="translate(336.5 31.5)"
                fill="none"
                stroke="#fff"
                stroke-linecap="round"
                stroke-width="2"
              />
              <line
                x2="24"
                transform="translate(336.5 38.5)"
                fill="none"
                stroke="#fff"
                stroke-linecap="round"
                stroke-width="2"
              />
            </g>
          </svg>
        </div>
        <div
          class="close-btn"
          v-if="activeNavbar"
          @click="activeNavbar = false"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="21"
            height="21"
            viewBox="0 0 21 21"
          >
            <path
              d="M28.5,9.615,26.385,7.5,18,15.885,9.615,7.5,7.5,9.615,15.885,18,7.5,26.385,9.615,28.5,18,20.115,26.385,28.5,28.5,26.385,20.115,18Z"
              transform="translate(-7.5 -7.5)"
            />
          </svg>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ContactBtn from "../components/ButtonMain.vue";

export default {
  name: "Navbar",
  components: { ContactBtn },
  data() {
    return {
      activeNavbar: false,
    };
  },
  methods: {
    scroll(id) {
      document.getElementById(id).scrollIntoView({
        behavior: "smooth",
      });
      this.activeNavbar = false;
    },
  },
  watch: {
    activeNavbar() {
      if (this.activeNavbar) {
        document.documentElement.style.overflow = "hidden";
        return;
      }
      document.documentElement.style.overflow = "auto";
    },
  },
};
</script>

<style lang="scss" scoped>
.container {
  background-color: none;
  z-index: 9999;
  width: 100%;
  margin: 0;
  display: grid;
  place-items: center;
  position: absolute;
  .navigation {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 80%;
    padding-top: 3.3rem;
    .logo {
      display: grid;
      place-items: center;
      font-size: 1.3rem;
      text-transform: capitalize;
      color: $darkblue;
      letter-spacing: 0.1rem;
    }
    .navigation__links {
      display: flex;
      list-style: none;
      li {
        padding-right: 1.8rem;
        color: $white;
        font-size: 1.3rem;
        text-transform: uppercase;
        letter-spacing: 0.1rem;
        transition-duration: 0.3s;
        &:hover {
          color: $purple;
          opacity: 0.6;
          cursor: pointer;
        }
      }
      .navigation__links-action {
        display: none;
      }
    }
    .close-btn {
      display: none;
    }
    .navigation__menu {
      display: none;
    }
  }
}

@media only screen and (max-width: 80rem) {
  .container {
    .navigation {
      .navigation__links {
        li {
          font-size: 0.8rem;
        }
      }
    }
  }
}

@media only screen and (max-width: 48rem) {
  .container {
    .navigation {
      width: 100%;
      margin: 0;
      padding: 0;
      position: relative;
      .logo {
        position: absolute;
        font-size: 1rem;
        top: 2rem;
        left: 2rem;
      }
      .navigation__links {
        display: none;
        li {
          font-size: 0.8rem;
        }
        .navigation__links-action {
          display: block;
        }
      }

      .navigation__menu {
        position: absolute;
        right: 2rem;
        top: 2rem;
        display: block;
        padding: 0.4rem;
        margin: 0;
        &:hover {
          cursor: pointer;
        }
      }
      .nav__menu {
        display: flex;
        flex-direction: column;
        align-items: flex-end;
        position: absolute;
        top: 0;
        right: 0;
        margin: 0;
        padding: 0;
        width: 100%;
        height: 100vh;
        background: $darkblue;
        transition: 0.2s ease-out;
        z-index: 3000;
        overflow-y: hidden;
        li {
          margin-top: 2rem;
          margin-right: 1rem;
        }
        li:nth-child(1) {
          margin-top: 8rem;
        }
      }
      .close-btn {
        position: absolute;
        display: block;
        top: 2rem;
        right: 2rem;
        width: 2rem;
        height: 100%;
        z-index: 4000;
        &:hover svg path {
          cursor: pointer;
          fill: $purple;
          transition: all 0.5s ease-out;
        }
      }
      .close-btn svg path {
        fill: $white;
      }
      .call-action {
        display: none;
      }
    }
  }
}
</style>