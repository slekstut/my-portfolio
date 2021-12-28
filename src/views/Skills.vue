<template>
  <div>
    <div class="container">
      <div class="wrapper">
        <h1>Skills</h1>
        <div class="skill-icon">
          <img src="../assets/icons/Icon-ionic-logo-html5.svg" alt="html5" />
          <img src="../assets/icons/Icon-simple-css3.svg" alt="css3" />
          <img src="../assets/icons/tailwind-css.svg" alt="tailwind" />
          <img src="../assets/icons/Icon-awesome-sass.svg" alt="sass" />
          <img src="../assets/icons/Icon-awesome-js.svg" alt="js" />
          <img src="../assets/icons/Icon-simple-vuejs.svg" alt="vue" />
          <img src="../assets/icons/Icon-awesome-node.svg" alt="node" />
          <img src="../assets/icons/adobe-xd.svg" alt="adobe-xd" />
          <img src="../assets/icons/figma-1.svg" alt="figma" />
          <img src="../assets/icons/git.svg" alt="" />
        </div>
        <div class="grid">
        <img src="../assets/icons/Repeat-Grid-5.svg" alt="">
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
  margin-top: 20%;
  width: 100%;
  display: grid;
  place-items: center;
  .wrapper {
    width: 80%;
    position: relative;
    h1 {
      font-size: 5rem;
      font-weight: 600;
      margin-bottom: 7.5rem;
      text-transform: capitalize;
    }
    .skill-icon {
    width: 80%;
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 5rem;
      justify-items: center;
      align-items: center;
    }
    .grid {
        position: absolute;
        top: 16rem;
        right: -53rem;
    }
  }
}
</style>