<template>
  <div>
    <div class="container">
      <div class="wrapper">
        <h4>Portfolios</h4>
        <h1>some of my latest projects</h1>
        <div class="projects">
          <img src="../assets/img/project-1.png" alt="project-1" />
          <img src="../assets/img/project-2.png" alt="project-2" />
          <img src="../assets/img/project-2.png" alt="project-2" />
          <img src="../assets/img/project-2.png" alt="project-2" />
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
  display: grid;
  justify-items: center;
  position: relative;
  .wrapper {
    width: 80%;
    text-align: center;
    display: grid;
    place-items: center;
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
    .projects {
      display: grid;
      grid-template-columns: minmax(10rem, 25rem) repeat(2, 1fr);
      gap: 1rem;
      justify-content: center;
      align-items: center;
      width: 80%;
      max-height: 100%;
      margin: 13rem 0;
      img {
        width: 100%;
        max-width: 25rem;
        justify-self: center;
      }
    }
  }
}
</style>