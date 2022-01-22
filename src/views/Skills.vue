<template>
  <div>
    <div class="container">
      <div class="wrapper">
        <h1>Skills</h1>
        <div class="skills">
          <div>
            <img src="../assets/icons/Icon-ionic-logo-html5.svg" alt="html5" />
            <p>HTML</p>
          </div>
          <div>
            <img src="../assets/icons/Icon-simple-css3.svg" alt="css3" />
            <p>css</p>
          </div>
          <div>
            <img src="../assets/icons/tailwind-css.svg" alt="tailwind" />
            <p>tailwind</p>
          </div>
          <div>
            <img src="../assets/icons/Icon-awesome-sass.svg" alt="sass" />
            <p>SASS</p>
          </div>
          <div>
            <img src="../assets/icons/js-icon.png" alt="js" />
            <p>javascript</p>
          </div>
          <div>
            <img src="../assets/icons/Icon-simple-vuejs.svg" alt="vue" />
            <p>vue js</p>
          </div>
          <div>
            <img src="../assets/icons/Icon-awesome-node.svg" alt="node" />
            <p>node js</p>
          </div>
          <div>
            <img src="../assets/img/adobe-xd.png" alt="adobe-xd" />
            <p>adobe xd</p>
          </div>
          <div>
            <img src="../assets/icons/figma-1.svg" alt="figma" />
            <p>figma</p>
          </div>
          <div>
            <img src="../assets/icons/git.svg" alt="" />
            <p>git</p>
          </div>
        </div>
        <div class="grid">
          <img src="../assets/icons/Repeat-Grid-5.svg" alt="" />
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
  margin-top: 10rem;
  margin-bottom: 5rem;
  width: 100%;
  display: grid;
  place-items: center;
  position: relative;
  .wrapper {
    width: 80%;
    position: relative;
    h1 {
      color: $black;
      font-size: 5rem;
      font-weight: 600;
      margin: 0;
      margin-bottom: 7.5rem;
      text-transform: capitalize;
    }
    .skills {
      width: 80%;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(15rem, 1fr));
      gap: 1rem;
      justify-items: center;
      align-items: center;
      div {
        display: grid;
        img {
          width: 5rem;
          height: 100%;
          align-self: center;
          justify-self: center;
        }
        p {
          font-size: 1.5rem;
          font-weight: 200;
          color: $black;
          text-transform: uppercase;
          text-align: center;
        }
      }
    }
    .grid {
      position: absolute;
      top: 16rem;
      right: -55rem;
    }
  }
}

@media only screen and (max-width: 80rem) {
  .container {
    .wrapper {
      h1 {
        font-size: 3rem;
      }
      .skills {
        width: 100%;
        grid-template-columns: repeat(auto-fit, minmax(15rem, 1fr));
      }
      .grid {
        position: absolute;
        right: -68rem;
      }
    }
  }
}

@media only screen and (max-width: 64rem) {
  .container {
    .wrapper {
      h1 {
        text-align: center;
      }
    }
  }
}

@media only screen and (max-width: 48rem) {
  .container {
    margin: 6rem 0;
    .wrapper {
      h1 {
          margin-bottom: 6rem;
        }
      .skills {
        grid-template-columns: repeat(auto-fit, minmax(8rem, 1fr));
        
        div p {
          font-size: 1rem;
        }
        div img {
          width: 3rem;
        }
      }
      .grid {
        display: none;
      }
    }
  }
}
</style>