<template>
  <div>
    <form>
      <div class="floating-label">
        <input class="floating-input" type="text" placeholder=" " />
        <span class="highlight"></span>
        <label>your email</label>
      </div>

      <div class="floating-label">
        <textarea
          class="floating-input floating-textarea"
          placeholder=" "
                  ></textarea>
        <span class="highlight"></span>
        <label>your message</label>
      </div>
      <button>send</button>
    </form>
  </div>
</template>

<script>
export default {
    name: "Form"
};
</script>

<style lang="scss" scoped>
form {
  width: 35%;
  .floating-label {
    position: relative;
    margin-bottom: 1.3rem;

  }
  .floating-input {
    font-size: 1.7rem;
    font-family: $font;
    font-weight: 300;
    letter-spacing: .15rem;
    color: $white;
    padding: 0.1rem 0;
    margin-bottom: 4rem;
    display: block;
    width: 100%;
    height: 3.2rem;
    background-color: transparent;
    border: none;
    border-bottom: 1px solid $white;
  }
  .floating-input:focus {
    outline: none;
    border-bottom: 2px solid $graylight;
  }

  label {
    color: $graylight;
    font-family: $font;
    font-size: 1.5rem;
    font-weight: 400;
    text-transform: capitalize;
    position: absolute;
    pointer-events: none;
    left: 5px;
    top: 5px;
    transition: 0.2s ease all;
    -moz-transition: 0.2s ease all;
    -webkit-transition: 0.2s ease all;
  }
  .floating-input:focus ~ label,
  .floating-input:not(:placeholder-shown) ~ label {
    top: -2rem;
    font-size: 1.2rem;
    color: $white;
  }
  .floating-input:focus ~ .bar:before,
  .floating-input:focus ~ .bar:after {
    width: 50%;
  }
  .floating-textarea {
    font-family: $font;
    overflow: scroll;
    min-height: 5rem;
    max-height: 20rem;
    overflow: hidden;
    overflow-x: hidden;
  }
  .highlight {
    position: absolute;
    height: 50%;
    width: 100%;
    top: 15%;
    left: 0;
    pointer-events: none;
    opacity: 0.5;
  }
  .floating-input:focus ~ .highlight {
    -webkit-animation: 0.3s ease;
    -moz-animation: 0.3s ease;
    animation: 0.3s ease;
  }
  button {
    margin-top: 2rem;
  }
}
</style>