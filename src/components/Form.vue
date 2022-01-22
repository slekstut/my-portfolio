<template>
  <form id="form-a" @submit.prevent="sendEmail">
    <div class="floating-label">
      <input
        class="floating-input"
        type="text"
        placeholder=" "
        name="name"
        v-model="state.name"
      />
      <span class="highlight"></span>
      <label>Name</label>
      <div :class="{ error: v$.name.$errors.length }">
        <div v-for="error of v$.name.$errors" :key="error.$uid">
          <div class="error-msg">{{ error.$message }}</div>
        </div>
      </div>
    </div>
    <div class="floating-label">
      <input
        class="floating-input"
        type="email"
        placeholder=" "
        name="email"
        v-model="state.email"
      />
      <span class="highlight"></span>
      <label>email</label>
      <div :class="{ error: v$.email.$errors.length }">
        <div v-for="error of v$.email.$errors" :key="error.$uid">
          <div class="error-msg">{{ error.$message }}</div>
        </div>
      </div>
    </div>
    <div class="floating-label">
      <textarea
        class="floating-input floating-textarea"
        placeholder=" "
        name="message"
        v-model="state.message"
      ></textarea>
      <span class="highlight"></span>
      <label>your message</label>
      <div :class="{ error: v$.message.$errors.length }">
        <div v-for="error of v$.message.$errors" :key="error.$uid">
          <div class="error-msg">{{ error.$message }}</div>
        </div>
      </div>
    </div>
    <div v-if="!state.isLoading">
      <input type="submit" value="Send" class="submit-btn" />
    </div>
    <div v-if="state.isLoading">
      <input
        type="submit"
        value="Sending..."
        class="submit-btn"
        :class="{ disabled: state.isLoading }"
      />
    </div>
    <div v-if="state.successMsg" class="success-message">
      <span>
        <svg
          aria-hidden="true"
          focusable="false"
          data-prefix="fas"
          data-icon="check"
          class="svg-inline--fa fa-check fa-w-16"
          role="img"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 512 512"
        >
          <path
            fill="currentColor"
            d="M173.898 439.404l-166.4-166.4c-9.997-9.997-9.997-26.206 0-36.204l36.203-36.204c9.997-9.998 26.207-9.998 36.204 0L192 312.69 432.095 72.596c9.997-9.997 26.207-9.997 36.204 0l36.203 36.204c9.997 9.997 9.997 26.206 0 36.204l-294.4 294.401c-9.998 9.997-26.207 9.997-36.204-.001z"
          ></path></svg
      ></span>
      <span
        >Thank you! Your message is sent successfully, I will contact you
        ASAP.</span
      >
    </div>
    <p>
      Or email me:
      <a href="mailto:sarunas.lekstutis@gmail.com" target="_blank"
        >sarunas.lekstutis@gmail.com</a
      >
    </p>
  </form>
</template>

<script>
import emailjs from "@emailjs/browser";
import { reactive } from "vue";
import useVuelidate from "@vuelidate/core";
import { required, email } from "@vuelidate/validators";

export default {
  name: "Form",
  setup() {
    const state = reactive({
      name: "",
      email: "",
      message: "",
      isLoading: false,
      successMsg: false,
    });
    const rules = {
      name: { required },
      email: { required, email },
      message: { required },
    };

    const v$ = useVuelidate(rules, state);

    return { state, v$ };
  },
  methods: {
    async sendEmail() {
      this.state.isLoading = true;
      const result = await this.v$.$validate();
      if (!result) {
        console.log("some error");
        this.state.isLoading = false;
        return;
      } else {
        setTimeout(() => {
          emailjs
            .sendForm(
              process.env.VUE_APP_MY_SERVICE_ID,
              process.env.VUE_APP_MY_TEMPLATE_ID,
              "#form-a",
              process.env.VUE_APP_MY_USER_ID
            )
            .then(
              (result) => {
                console.log("SUCCESS!", result.text);
              },
              (error) => {
                console.log("FAILED...", error.text);
              }
            );
          this.state.isLoading = false;
          this.state.successMsg = true;
          this.resetForm();
        }, 2000);
        setTimeout(() => {
          this.state.successMsg = false;
        }, 10000);
      }
    },
    async resetForm() {
      const result = await this.v$.$reset();
      if (!result) {
        this.state.name = "";
        this.state.email = "";
        this.state.message = "";
      }
    },
  },
};
</script>

<style lang="scss" scoped>
form {
  width: 50%;
  display: grid;
  grid-template-columns: 1fr;
  gap: 4rem;
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
  .submit-btn {
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
    border: 1px solid $white;
    border-radius: 1.2rem;
    padding: 1rem 1.5rem;
    color: $white;
    font-weight: 700;
    letter-spacing: 0.1rem;
    text-transform: capitalize;
    transition-duration: 0.3s;
    &:hover {
      background-color: $white;
      color: $purple;
      cursor: pointer;
      transition-duration: 0.3s;
    }
  }
  .disabled {
    pointer-events: none;
  }
  p {
    font-size: 1.2rem;
    text-align: center;
    color: $white;
    margin: 2rem 0;
    a {
      font-size: 1.2rem;
      color: $white;
      text-decoration: underline;
    }
  }
}

@media only screen and (max-width: 80rem) {
  form {
    width: 65%;
  }
}

@media only screen and (max-width: 64rem) {
  form {
    gap: 2rem;
    margin: 0 auto;
    .floating-input {
      font-size: 1.2rem;
    }
    label {
      font-size: 1.2rem;
    }
    .floating-input:focus ~ label,
    .floating-input:not(:placeholder-shown) ~ label {
      font-size: 1rem;
    }
    .floating-textarea {
      font-size: 1.2rem;
    }
    p {
      font-size: 1.2rem;
      margin: 1.2rem 0;
    }
  }
}

@media only screen and (max-width: 48rem) {
  form {
    width: 80%;
    .submit-btn {
      font-size: 1.2rem;
      font-weight: 400;
      padding: 0.8rem 1.2rem;
    }
    p {
      font-size: 0.7rem;
      font-weight: 200;
      margin: .8rem 0;
      a {
        font-size: 0.7rem;
        font-weight: 200;
      }
    }
  }
}

@media only screen and (max-width: 37.5rem) {
  form {
    .floating-input {
      font-size: 0.8rem;
    }
    label {
      font-size: 0.8rem;
    }
    .floating-input:focus ~ label,
    .floating-input:not(:placeholder-shown) ~ label {
      font-size: 0.6rem;
    }
    .floating-textarea {
      font-size: 0.8rem;
    }
  }
}
</style>