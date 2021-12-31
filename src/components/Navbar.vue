<template>
  <div>
    <div class="container">
      <div class="wrapper">
        <div class="logo">Sarunas Lekstutis</div>
        <ul>
          <li>home</li>
          <li>services</li>
          <li>projects</li>
          <li>about</li>
        </ul>
        <div class="contact">
          <button>contact me</button>
        </div>
        <div class="hamburger">
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
      </div>
    </div>
  </div>
</template>

<script>
export default {};
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
    width: 80%;
    padding-top: 3.3rem;
    .logo {
      display: grid;
      place-items: center;
      font-size: 1.3rem;
      text-transform: capitalize;
      color: $white;
      letter-spacing: 0.1rem;
    }
    ul {
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
</style>