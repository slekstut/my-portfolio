<template>
  <div>
    <div class="container">
      <div class="wrapper">
        <div class="logo">Sarunas Lekstutis</div>
        <ul class="nav" :class="{ 'mobile-menu': activeNavbar }">
          <li>home</li>
          <li>services</li>
          <li>projects</li>
          <li>about</li>
        </ul>
        <div class="contact">
          <button>contact me</button>
        </div>
        <div
          class="hamburger"
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
        <div class="close-btn" v-else @click="activeNavbar = false">
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
export default {
  name: "Navbar",
  data() {
    return {
      activeNavbar: true,
    };
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
  .wrapper {
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
    .nav {
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
    }

    .contact {
      display: grid;
      place-items: center;
      button {
        height: 100%;
        background: $darkblue;
        font-size: 1.3rem;
        border: 1px solid transparent;
        border-radius: 25px;
        text-transform: uppercase;
        padding: 0.5rem 1.5rem;
        color: $white;
        font-weight: 700;
        letter-spacing: 0.1rem;
        text-transform: capitalize;
        transition-duration: 0.3s;
        white-space: nowrap;
        &:hover {
          background-color: $white;
          color: $purple;
          cursor: pointer;
        }
      }
    }
    .hamburger {
      display: none;
    }
  }
}

@media only screen and (max-width: 80rem) {
  .container {
    .wrapper {
      .nav {
        li {
          font-size: 0.8rem;
        }
      }
      .contact {
        button {
          font-size: 0.8rem;
          text-transform: uppercase;
        }
      }
    }
  }
}

@media only screen and (max-width: 48rem) {
  .container {
    position: relative;
    .wrapper {
      width: 100%;
      margin: 0;
      padding: 0;
      .logo {
        position: absolute;
        top: 2rem;
        left: 2rem;
      }
      .nav {
        display: none;
        li {
          font-size: 0.8rem;
        }
      }
      .contact {
        button {
          display: none;
          opacity: 0;
          visibility: hidden;
        }
      }
      .hamburger {
        position: absolute;
        right: 2rem;
        top: 2rem;
        display: block;
        float: right;
        padding: 0.4rem;
        margin: 0;
        &:hover {
          cursor: pointer;
        }
      }
      .mobile-menu {
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
    }
  }
}
</style>