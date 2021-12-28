<template>
  <div>
    <div class="container">
      <div class="wrapper">
        <div>
          <h1>about me</h1>
          <p>
            Self-taught front end web developer seeking full-time developer role
            at starting position or part time job. Expierence in my personal
            projects and current role in project management area will bring the
            most value and satisfaction to my employer and the end user.
          </p>
          <button>download cv</button>
        </div>
        <div class="portfolio-image">
          <img src="../assets/img/foto.png" alt="my-photo" />
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
  margin-top: 25%;
  width: 100%;
  display: grid;
  place-items: center;
  .wrapper {
    width: 80%;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2rem;
    h1 {
      font-size: 5rem;
      font-weight: 600;
      margin-bottom: 7.5rem;
      text-transform: capitalize;
    }
    p {
      font-size: 1.8rem;
      text-align: left;
      margin: 0;
      line-height: 2.8rem;
    }
    button {
      background-color: $darkblue;
      color: $white;
      margin-top: 7.5rem;
      font-size: 1.8rem;
      padding: 2rem 2.5rem;
      text-transform: uppercase;
      letter-spacing: 0.25rem;
      border: 1px solid transparent;
      font-weight: 400;
      width: 100%;
      &:hover {
        color: $darkblue;
        background-color: $white;
        border: 1px solid $darkblue;
        font-weight: 400;
        cursor: pointer;
        transition: all 0.5s ease-out;
      }
    }
    .portfolio-image {
      justify-self: center;
      align-self: center;
      z-index: 1000;
      img {
        width: 50%;
      }
    }
  }
}
</style>