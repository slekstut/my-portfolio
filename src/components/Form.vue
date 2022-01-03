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
      <button>
        send<span
          ><svg
            xmlns="http://www.w3.org/2000/svg"
            width="33.621"
            height="33.621"
            viewBox="0 0 33.621 33.621"
          >
            <g transform="translate(-1.5 -0.879)">
              <path
                d="M33,3,16.5,19.5"
                fill="none"
                stroke="#fff"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="3"
              />
              <path
                d="M33,3,22.5,33l-6-13.5L3,13.5Z"
                fill="none"
                stroke="#fff"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="3"
              />
            </g></svg
        ></span>
      </button>
    </form>
  </div>
</template>

<script>
export default {
  name: "Form",
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
    letter-spacing: 0.05rem;
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
    min-height: 8rem;
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
    display: inline-flex;
    flex-wrap: nowrap;
    gap: 1.2rem;
    align-items: center;
    justify-content: center;  
    width: 100%;
    margin-top: 1.5rem;
    background: transparent;
    font-size: 1.3rem;
    text-transform: uppercase;
    border: 2px solid $white;
    border-radius: 1.2rem;
    padding: 1rem 1.5rem;
    color: $white;
    font-weight: 700;
    letter-spacing: 0.1rem;
    text-transform: capitalize;
    transition-duration: 0.3s;
    &:hover span svg path{
        stroke: $purple;
    }
    &:hover {
      background-color: $white;
      color: $purple;
      cursor: pointer;
    }
  }
}
</style>