<template>
  <div>
    <div class="container">
      <div class="wrapper">
        <div class="text">
          <h1>Hello this is Sarunas</h1>
          <h3>front end developer</h3>
        </div>
        <div class="socials">
          <img
            src="../assets/icons/linkedin-socials.svg"
            alt="linkedin-facebook"
          />
          <img src="../assets/icons/github-socials.svg" alt="github-facebook" />
          <img
            src="../assets/icons/facebook-socials.svg"
            alt="socials-facebook"
          />
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
  height: 64rem;
  width: 100%;
  padding-top: 3%;
  top: 0;
  position: relative;
  background-image: url("../assets/img/background-image.png");
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  display: grid;
  place-items: center;
  .wrapper {
    width: 80%;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    .text {
    grid-column-start: 1;
    grid-column-end: 4;
    justify-self: center;
    h1 {
        color: $white;
        font-size: 5rem;
        margin: 0;
    }
    h3 {
        color: $white;
        font-size: 2rem;
        font-weight: 400;
        text-transform: capitalize;
    }
    }
    .socials {
    justify-self: end;
    display: flex;
    flex-direction: column;
    gap: 2rem;
        
    }
  }
}
</style>