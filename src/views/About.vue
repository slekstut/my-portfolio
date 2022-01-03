<template>
  <div>
    <div class="container">
      <div class="wrapper">
        <div>
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
          <button>download cv</button>
        </div>
        <div class="portfolio-image">
          <img src="../assets/img/my-portfolio-img-edited.png" alt="my-photo" />
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
  margin-top: 8%;
  width: 100%;
  display: grid;
  place-items: center;
  .wrapper {
    width: 80%;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 8rem;
    h1 {
      font-size: 5rem;
      color: $black;
      font-weight: 600;
      line-height: 0.8;
      margin: 0;
      margin-bottom: 7.5rem;
      text-transform: capitalize;
    }
    p {
      font-size: 1.8rem;
      color: $black;
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
      border-radius: 1.2rem;
      font-weight: 400;
      width: 100%;
      &:hover {
        color: $darkblue;
        background-color: $white;
        border: 1px solid $darkblue;
        border-radius: 1.2rem;
        font-weight: 400;
        cursor: pointer;
        transition: all 0.5s ease-out;
      }
    }
    .portfolio-image {
      display: flex;
      place-items: center;
      z-index: 1000;
      img {
        width: 100%;
      }
    }
  }
}
</style>