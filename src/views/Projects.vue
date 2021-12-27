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
  height: 100vh;
  width: 100%;
  display: grid;
  place-items: center;
  .wrapper {
    width: 80%;
    display: grid;
    place-items: center;
    h4 {
      color: $white;
      margin-top: 10rem;
      font-size: 1.65rem;
      font-weight: 200;
      letter-spacing: 0.2rem;
      text-transform: uppercase;
    }
    h1 {
      color: $white;
      font-size: 5rem;
      font-weight: 600;
      margin: 2rem 0 7.5rem 0;
      text-transform: uppercase;
    }
  }
}
</style>