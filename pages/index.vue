<template>
  <div class="l-container">
    <div>
      <Logo />
      <div class="l-links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          rel="noopener noreferrer"
          class="button--green"
        >
          Documentation
        </a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          rel="noopener noreferrer"
          class="button--grey"
        >
          GitHub
        </a>
      </div>
      <h1 class="c-title">
        welcome, Nuxt.js
      </h1>
    </div>
    <div class="c-water">
      <svg class="c-water__waterwave c-water__back" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 749.866 619.483">
      <path id="path_11" class="cls-1" d="M.127-35.3S50.2,6.431,99.143,6.489,164.71-12.845,193.368-35.1s53.288-29.32,96.2-29.058,85.049,29.274,85.049,29.274l.626,590.2L-.626,555.21Z" transform="translate(374.626 64.167)" />
        <path id="path_21" class="cls-1" d="M.127-35.3S50.2,6.431,99.143,6.489,164.71-12.845,193.368-35.1s53.288-29.32,96.2-29.058,85.049,29.274,85.049,29.274l.626,590.2L-.626,555.21Z" transform="translate(0.626 64.167)" />
      </svg>
      <svg class="c-water__waterwave c-water__center" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 749.866 619.483">
      <path id="path_11" class="cls-1" d="M.127-35.3S50.2,6.431,99.143,6.489,164.71-12.845,193.368-35.1s53.288-29.32,96.2-29.058,85.049,29.274,85.049,29.274l.626,590.2L-.626,555.21Z" transform="translate(374.626 64.167)" />
        <path id="path_21" class="cls-1" d="M.127-35.3S50.2,6.431,99.143,6.489,164.71-12.845,193.368-35.1s53.288-29.32,96.2-29.058,85.049,29.274,85.049,29.274l.626,590.2L-.626,555.21Z" transform="translate(0.626 64.167)" />
      </svg>
      <svg class="c-water__waterwave c-water__front" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 749.866 619.483">
      <g transform="translate(0.126 -192.333)">
        <path id="path_1" class="cls-1" d="M374.487-35.3S324.41,6.431,275.472,6.489,209.905-12.845,181.247-35.1s-53.288-29.32-96.2-29.058S0-34.885,0-34.885l-.626,590.2,375.866-.107Z" transform="translate(0.5 256.5)" />
        <path id="path_2" class="cls-1" d="M374.487-35.3S324.41,6.431,275.472,6.489,209.905-12.845,181.247-35.1s-53.288-29.32-96.2-29.058S0-34.885,0-34.885l-.626,590.2,375.866-.107Z" transform="translate(374.5 256.5)" />
      </g>
      </svg>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.l {
  &-container {
    margin: 0 auto;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
  }
  &-links {
    padding-top: 15px;
  }
}

.c {
  &-water {
    position: fixed;
	  transition: all 1s ease-out;
    top: 60%;
    height: 100%;
    width: 100%;
    z-index: -1;
  }
  &-water__waterwave {
    position: absolute;
    top: 0;
    width: 200%;
  }
  &-water__back,
  &-water__center,
  &-water__front {
    animation-fill-mode: none;
    animation-timing-function: linear;
    animation-iteration-count: infinite;
  }
  &-water__back {
    fill: #00C58E;
    left: 0;
    animation-duration: 20s;
    animation-name: wavegrad-back;
  }
  &-water__center {
    fill: #2F495E;
    left: 0;
    top: 10%;
    animation-duration: 40s;
    animation-name: wavegrad-back;
  }
  &-water__front {
    fill: #108775;
    left: -50;
    animation-duration: 20s;
    animation-name: wavegrad;
  }
  &-title {
    font-family:
      'Quicksand',
      'Source Sans Pro',
      -apple-system,
      BlinkMacSystemFont,
      'Segoe UI',
      Roboto,
      'Helvetica Neue',
      Arial,
      sans-serif;
    display: block;
    font-weight: 300;
    font-size: 100px;
    color: #31364ae8;
    letter-spacing: 1px;
    margin-top: 20px;
  }
}

@keyframes wavegrad {
  0% {
    left: -100%;
    top: 0%;
  }

  50% {
    top: 3%;
  }

  100% {
    left: 0%;
    top: 0%;
  }
}

@keyframes wavegrad-back {
  from {
    left: 0%;
  }

  to {
    left: -100%;
  }
}

</style>
