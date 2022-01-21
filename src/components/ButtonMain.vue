<template>
  <div class="main-btn">
    <a
      href="https://drive.google.com/file/d/1tnCvAHHN5hw6DBJZVVF4uE70zDL81xut/view?usp=sharing"
      target="_blank"
      ><slot></slot
    ></a>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.main-btn {
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  margin-left: 0;
  width: fit-content;
  padding: 0.85rem 2rem;
  border-radius: 1.2rem;
  background-color: $darkblue;
  white-space: nowrap;
  box-shadow: 14px 14px 44px -1px rgba(59, 68, 75, 0.29);
  -webkit-box-shadow: 14px 14px 44px -1px rgba(59, 68, 75, 0.29);
  -moz-box-shadow: 14px 14px 44px -1px rgba(59, 68, 75, 0.29);
  a {
    display: inline-block;
    color: $white;
    font-size: 1.2rem;
    text-transform: uppercase;
    letter-spacing: 0.1rem;
    font-weight: 400;
    text-decoration: none;
  }
  &:hover {
    background-color: $white;
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

@media only screen and (max-width: 80rem) {
  .main-btn {
    padding: 0.65rem 1.75rem;
    a {
      font-size: 0.8rem;
    }
  }
}

@media only screen and (max-width: 48rem) {
  .main-btn {
    margin: 0 auto;
  }
}
</style>