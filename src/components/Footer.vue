<template>
  <footer><div><p>2022 Sarunas Lekstutis</p></div></footer>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
footer {
  clear: both;
  position: relative;
  height: 8rem;
  margin-top: -8rem;
  display: grid;
  place-items: center;
  width: 100%;
  div {
  width: 80%;
    border-top: 1px solid $graylighter;
    p {
    color: $white;
    font-size: 1rem;
    font-weight: 200;
    letter-spacing: 0.1rem;
    text-align: center;
  }
  }
  
}
</style>