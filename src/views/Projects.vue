<template>
  <div>
    <div class="container">
      <div class="wrapper">
        <h4>Portfolios</h4>
        <h1>some of my latest projects</h1>
        <div class="slider__wrapper">
          <div class="left-arrow">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="100"
              height="100"
              viewBox="0 0 100 100"
            >
              <path
                d="M100,50A50,50,0,1,1,50,0,50,50,0,0,1,100,50ZM52.214,66.539a3.129,3.129,0,1,1-4.425,4.425l-18.75-18.75a3.125,3.125,0,0,1,0-4.425l18.75-18.75a3.129,3.129,0,1,1,4.425,4.425L38.794,46.875H68.75a3.125,3.125,0,1,1,0,6.25H38.794L52.214,66.539Z"
                fill="rgba(255,255,255,0.3)"
                fill-rule="evenodd"
              />
            </svg>
          </div>
          <div class="img-slider">
            <img src="../assets/img/project-1.png" alt="project-1" />
            <img src="../assets/img/project-2.png" alt="project-2" />
          </div>
          <div class="right-arrow">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="100"
              height="100"
              viewBox="0 0 100 100"
            >
              <path
                d="M100,50A50,50,0,1,1,50,0,50,50,0,0,1,100,50ZM47.789,66.539a3.129,3.129,0,1,0,4.425,4.425l18.75-18.75a3.125,3.125,0,0,0,0-4.425l-18.75-18.75a3.129,3.129,0,1,0-4.425,4.425L61.206,46.875H31.25a3.125,3.125,0,1,0,0,6.25H61.206L47.786,66.539Z"
                fill="rgba(255,255,255,0.3)"
                fill-rule="evenodd"
              />
            </svg>
          </div>
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
  background-color: $darkblue;
  width: 100%;
  height: 70rem;
  display: grid;
  justify-items: center;
  position: relative;
  .wrapper {
    width: 80%;
    text-align: center;
    h4 {
      color: $white;
      font-size: 1.65rem;
      margin-top: 10rem;
      font-weight: 200;
      letter-spacing: 0.2rem;
      text-transform: uppercase;
    }
    h1 {
      color: $white;
      font-size: 5rem;
      font-weight: 600;
      margin: 0;
      text-transform: uppercase;
    }
    .slider__wrapper {
      display: grid;
      grid-template-columns: 10% 80% 10%;
      gap: 2rem;
      position: absolute;
      left: 50%;
      transform: translate(-50%, 0);
      bottom: -10rem;
      justify-content: space-between;
      width: 80%;
      .img-slider {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 3rem;
        align-items: center;
        img {
          max-width: 38rem;
          height: 100%;
        }
      }
      .left-arrow {
        justify-self: start;
        align-self: center;
        &:hover svg path {
          fill: $white;
          transition: all 0.5s ease-out;
          cursor: pointer;
        }
      }
      .right-arrow {
        justify-self: end;
        align-self: center;
        &:hover svg path {
          fill: $white;
          transition: all 0.5s ease-out;
          cursor: pointer;
        }
      }
    }
  }
}
</style>