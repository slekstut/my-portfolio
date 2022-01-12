<template>
  <div>
    <div class="container" id="home">
      <div class="wrapper">
        <div class="text">
          <h1>Hello this is Sarunas</h1>
          <h3>front end developer</h3>
          <a @click="scroll('projects')"
            ><button class="call-action">check my projects</button></a
          >
        </div>
        <div class="socials">
          <a
            href="https://www.linkedin.com/in/sarunas-lekstutis-296854108/"
            target="_blank"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="80"
              height="80"
              viewBox="0 0 80 80"
            >
              <defs>
                <svg:style>
                  .a {
                    fill: rgba(255, 255, 255, 0);
                    stroke: rgba(204, 190, 190, 0.2);
                    stroke-width: 2px;
                  }

                  .b {
                    fill: #ece5e5;
                  }

                  .c {
                    stroke: none;
                  }

                  .d {
                    fill: none;
                  }
                </svg:style>
              </defs>
              <g class="a">
                <circle class="c" cx="40" cy="40" r="40" />
                <circle class="d" cx="40" cy="40" r="39" />
              </g>
              <path
                class="b"
                d="M8.539,42.226H.63V14.041H8.539ZM4.58,10.2A4.889,4.889,0,0,1,0,5.079,4.843,4.843,0,0,1,4.58.01a4.843,4.843,0,0,1,4.58,5.069A4.889,4.889,0,0,1,4.58,10.2Zm33.56,32.03H30.248V28.505c0-3.27-.06-7.463-4.112-7.463-4.112,0-4.742,3.553-4.742,7.228V42.226h-7.9V14.041h7.585v3.845h.111a8.2,8.2,0,0,1,7.483-4.552c8,0,9.476,5.833,9.476,13.41V42.226Z"
                transform="translate(20.926 13.882)"
              /></svg
          ></a>
          <a href="https://github.com/slekstut" target="_blank">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="80"
              height="80"
              viewBox="0 0 80 80"
            >
              <defs>
                <svg:style>
                  .a {
                    fill: rgba(255, 255, 255, 0);
                    stroke: rgba(204, 190, 190, 0.2);
                    stroke-width: 2px;
                  }

                  .b {
                    fill: #ece5e5;
                  }

                  .c {
                    stroke: none;
                  }

                  .d {
                    fill: none;
                  }
                </svg:style>
              </defs>
              <g class="a">
                <circle class="c" cx="40" cy="40" r="40" />
                <circle class="d" cx="40" cy="40" r="39" />
              </g>
              <path
                class="b"
                d="M14.248,41.335c0,.171-.2.308-.447.308-.283.026-.481-.111-.481-.308,0-.171.2-.308.447-.308C14.025,41,14.248,41.138,14.248,41.335Zm-2.671-.385c-.06.171.112.368.369.419a.4.4,0,0,0,.532-.171c.052-.171-.112-.368-.369-.445A.441.441,0,0,0,11.577,40.95Zm3.8-.146c-.249.06-.421.223-.4.419.026.171.249.283.507.223s.421-.223.4-.394S15.622,40.779,15.373,40.8ZM21.025,8A20.561,20.561,0,0,0,0,28.888,21.468,21.468,0,0,0,14.557,49.365c1.1.2,1.486-.479,1.486-1.036,0-.531-.026-3.459-.026-5.256,0,0-6.012,1.284-7.274-2.551,0,0-.979-2.491-2.388-3.133,0,0-1.967-1.344.137-1.318a4.536,4.536,0,0,1,3.315,2.209c1.881,3.3,5.033,2.354,6.261,1.789a4.752,4.752,0,0,1,1.374-2.885c-4.8-.531-9.645-1.224-9.645-9.46a6.477,6.477,0,0,1,2.027-5.042,8.064,8.064,0,0,1,.223-5.813c1.795-.556,5.926,2.311,5.926,2.311a20.353,20.353,0,0,1,10.787,0s4.131-2.876,5.926-2.311a8.06,8.06,0,0,1,.223,5.813c1.374,1.515,2.216,2.7,2.216,5.042,0,8.261-5.059,8.92-9.86,9.46a5.054,5.054,0,0,1,1.46,3.972c0,2.885-.026,6.455-.026,7.157,0,.556.4,1.233,1.486,1.036A21.269,21.269,0,0,0,42.6,28.888C42.6,17.014,32.937,8,21.025,8ZM8.348,37.526c-.112.086-.086.283.06.445.137.137.335.2.447.086.112-.086.086-.283-.06-.445C8.657,37.474,8.46,37.415,8.348,37.526Zm-.928-.693c-.06.111.026.248.2.334a.256.256,0,0,0,.369-.06c.06-.111-.026-.248-.2-.334C7.618,36.721,7.481,36.747,7.42,36.832ZM10.2,39.88c-.137.111-.086.368.112.531.2.2.447.223.558.086.112-.111.06-.368-.112-.531C10.572,39.769,10.315,39.743,10.2,39.88Zm-.979-1.258c-.137.086-.137.308,0,.505s.369.283.481.2a.39.39,0,0,0,0-.531C9.585,38.6,9.361,38.51,9.224,38.622Z"
                transform="translate(18.701 11.3)"
              /></svg
          ></a>
          <a href="https://www.facebook.com/sarunas.lekstutis.5" target="_blank"
            ><svg
              xmlns="http://www.w3.org/2000/svg"
              width="80"
              height="80"
              viewBox="0 0 80 80"
              fill="currentColor"
            >
              <defs>
                <svg:style>
                  .a {
                    fill: rgba(255, 255, 255, 0);
                    stroke: rgba(204, 190, 190, 0.2);
                    stroke-width: 2px;
                  }

                  .b {
                    fill: #ece5e5;
                  }

                  .c {
                    stroke: none;
                  }

                  .d {
                    fill: none;
                  }
                </svg:style>
              </defs>
              <g class="a">
                <circle class="c" cx="40" cy="40" r="40" />
                <circle fill="currentColor" class="d" cx="40" cy="40" r="39" />
              </g>
              <path
                class="b"
                d="M43.341,22.628l1.135-7.28h-7.1V10.623c0-1.992.991-3.933,4.169-3.933h3.226V.492A39.942,39.942,0,0,0,39.049,0c-5.844,0-9.663,3.487-9.663,9.8v5.549h-6.5v7.28h6.5v17.6H37.38v-17.6Z"
                transform="translate(6.167 19.886)"
              /></svg
          ></a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    scroll(id) {
      document.getElementById(id).scrollIntoView({
        behavior: "smooth",
      });
    },
  },
};
</script>

<style lang="scss" scoped>
.container {
  height: 100vh;
  width: 100%;
  padding-top: 3%;
  top: -0.5rem;
  position: relative;
  background-image: url("../assets/img/bg-img.png");
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
      display: grid;
      justify-content: end;
      grid-template-rows: auto 1fr 1fr;
      h1 {
        align-self: end;
        justify-self: start;
        color: $darkblue;
        font-size: 10rem;
        font-weight: 600;
        margin: 0;
        text-align: left;
        line-height: 1;
      }
      h3 {
        display: inline-block;
        align-self: start;
        justify-self: start;
        color: $darkblue;
        font-size: 2rem;
        position: relative;
        font-weight: 400;
        text-transform: capitalize;
        margin: 0;
        text-align: center;
        letter-spacing: 0.1rem;
        &:hover::after {
          width: 100%;
          background: $purple;
        }
      }
      h3:after {
        content: "";
        position: absolute;
        background: $white;
        height: 3px;
        bottom: -3px;
        margin: 0;
        left: 0;
        right: 0;
        width: 12%;
        border-radius: 5px;
        transition: all 0.5s ease-out;
      }
      .call-action {
        display: none;
      }
    }
    .socials {
      justify-self: end;
      display: flex;
      flex-direction: column;
      gap: 2rem;
      a {
        svg {
          width: 3rem;
          &:hover {
            cursor: pointer;
          }
          &:hover .a {
            transition: all 1s ease-out;
            fill: $purple;
          }
        }
      }
    }
  }
}

@media only screen and (max-width: 80rem) {
  .container {
    .wrapper {
      .text {
        h1 {
          font-size: 7rem;
        }
        h3 {
          font-size: 1.5rem;
          margin-left: 0;
        }
        h3:after {
          width: 2rem;
        }
      }
    }
  }
}

@media only screen and (max-width: 64rem) {
  .container {
    .wrapper {
      .text {
        h1 {
          font-size: 6rem;
        }
      }
    }
  }
}

@media only screen and (max-width: 48rem) {
  .container {
    .wrapper {
      .text {
        h1 {
          text-align: center;
        }
        h3 {
          font-size: 1rem;
          justify-self: center;
        }
        h3:after {
          height: 1px;
        }
        a {
          margin: 0 auto;
          .call-action {
            display: inline-block;
            justify-self: center;
            width: auto;
            margin-top: 2rem;
            background: $darkblue;
            font-size: 0.8rem;
            border: 1px solid transparent;
            border-radius: 25px;
            text-transform: uppercase;
            padding: 1rem 2rem;
            color: $white;
            font-weight: 700;
            letter-spacing: 0.1rem;
            text-transform: capitalize;
            transition-duration: 0.3s;
            white-space: nowrap;
            &:hover {
              background-color: $white;
              color: $purple;
              cursor: pointer;
            }
          }
        }
      }
      .socials {
        gap: 0.5rem;
        a {
          svg {
            width: 2rem;
            height: 100%;
          }
        }
      }
    }
  }
}

@media only screen and (max-width: 43.75rem) {
  .container {
    .wrapper {
      .text {
        h1 {
          font-size: 4rem;
        }
        h3 {
          justify-self: center;
        }
      }
      .socials {
        gap: 0.5rem;
        a {
          svg {
            width: 2rem;
            height: 100%;
          }
        }
      }
    }
  }
}
</style>