<template>
  <div>
    <div class="container">
      <div class="wrapper" id="about">
        <div class="text">
          <h1>about me</h1>
          <p>
            I am from Lithuania. I started programming Pascal since school.
            Later I graduated with a bachelor's degree in computer engineering
            from Klaipeda University. After studying, I didn’t know what I
            wanted to do in my life, so fate ensued and I fell into a non-IT job
            where I still work. But after a few years, I realized I wanted to
            work as a website developer. Since then, I have been actively
            learning, programming and pursuing career change. I love programming
            and website design and everything related to it.
          </p>
          <div class="cv-btn">
            <a
              href="https://drive.google.com/file/d/1e6uEh4WakgVgT9XGDkCn4GGHeItjieRx/view?usp=sharing"
              target="_blank"
              >download cv</a
            >
          </div>
        </div>
        <div class="portfolio-image">
          <img src="../assets/img/my-portfolio-img-edited.png" alt="my-photo" />
        </div>
        <div class="about-bg"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.container {
  margin-top: 15rem;
  width: 100%;
  display: grid;
  place-items: center;
  position: relative;
  z-index: 0;
  .wrapper {
    width: 80%;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 8rem;
    .text {
      display: grid;
      grid-template-columns: 1fr;
      gap: 6rem;
      h1 {
        font-size: 5rem;
        color: $black;
        font-weight: 600;
        line-height: 0.8;
        margin: 0;
        text-transform: capitalize;
        white-space: nowrap;
      }
      p {
        font-size: 1.8rem;
        font-weight: 200;
        color: $black;
        text-align: left;
        margin: 0;
        line-height: 1.5;
        z-index: 0;
      }
      .cv-btn {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
        max-width: 50rem;
        max-height: 8rem;
        padding: 2rem 2.5rem;
        border: 1px solid transparent;
        border-radius: 1.2rem;
        background-color: $darkblue;
        box-shadow: 14px 14px 44px -1px rgba(59, 68, 75, 0.29);
        -webkit-box-shadow: 14px 14px 44px -1px rgba(59, 68, 75, 0.29);
        -moz-box-shadow: 14px 14px 44px -1px rgba(59, 68, 75, 0.29);
        a {
          color: $white;
          font-size: 1.8rem;
          text-transform: uppercase;
          letter-spacing: 0.25rem;
          font-weight: 400;
          text-decoration: none;
        }
        &:hover {
          background-color: $white;
          border: 1px solid $darkblue;
          border-radius: 1.2rem;
          cursor: pointer;
          transition: all 0.5s ease-out;
        }
        &:hover a {
          color: $darkblue;
          font-weight: 400;
          background-color: transparent;
        }
      }
    }
    .portfolio-image {
      display: grid;
      place-items: center;
      z-index: 1000;
      img {
        width: 100%;
      }
    }
  }
  .about-bg {
    position: absolute;
    background-image: url("../assets/img/About.svg");
    background-repeat: no-repeat;
    background-size: cover;
    width: 100%;
    height: 100%;
    max-height: 55rem;
    top: -15rem;
    right: -10rem;
    z-index: 3000;
  }
}

@media only screen and (max-width: 80rem) {
  .container {
    .wrapper {
      gap: 4rem;
      .text {
        gap: 3rem;
        h1 {
          margin-bottom: 3.5rem;
        }
        p {
          font-size: 1.2rem;
        }
        .cv-btn {
          padding: 1rem 1.25rem;
          margin-top: 3.5rem;
        }
      }
    }
    .about-bg {
      height: 30rem;
    }
  }
}

@media only screen and (max-width: 64rem) {
  .container {
    .wrapper {
      gap: 1.5rem;
      .text {
        gap: 2rem;
        p {
          font-size: 1.2rem;
        }
        .cv-btn {
          padding: 1rem 1.25rem;
        }
      }
    }
  }
}

@media only screen and (max-width: 48rem) {
  .container {
    .wrapper {
      grid-template-columns: 1fr;
      gap: 3.5rem;
      .text {
        p {
          font-size: 1.2rem;
        }
        .cv-btn {
          a {
            font-size: 1.2rem;
          }
        }
      }
    }
  }
}
</style>