<template>
  <div>
    <form class="floating-form">
      <div class="floating-label">
        <input class="floating-input" type="text" placeholder=" " />
        <span class="highlight"></span>
        <label>Text</label>
      </div>

      <div class="floating-label">
        <textarea
          class="floating-input floating-textarea"
          placeholder=" "
        ></textarea>
        <span class="highlight"></span>
        <label>Textarea</label>
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
.floating-form {
  width: 25rem;
  .floating-label {
    position: relative;
    margin-bottom: 20px;
  }
  .floating-input {
    font-size: 1.8rem;
    padding: 0.2rem;
    display: block;
    width: 100%;
    height: 30px;
    background-color: transparent;
    border: none;
    border-bottom: 1px solid $white;
  }
  .floating-input:focus {
    outline: none;
    border-bottom: 2px solid $graylight;
  }

  label {
    color: $white;
    font-size: 0.8rem;
    font-weight: 400;
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
    top: -18px;
    font-size: 14px;
    color: $white;
  }
  .floating-input:focus ~ .bar:before,
  .floating-input:focus ~ .bar:after,
  .floating-select:focus ~ .bar:before,
  .floating-select:focus ~ .bar:after {
    width: 50%;
  }
  .floating-textarea {
    min-height: 30px;
    max-height: 260px;
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
}
</style>