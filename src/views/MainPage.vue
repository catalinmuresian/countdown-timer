<template>
  <div class="main-page">
    <h1>We’re launching soon</h1>
    <div class="container">
      <div class="container-segment">
        <div class="segment">
          <div class="flip-card" ref="data_days">
            <div ref="top" class="top">14</div>
            <div ref="bottom" class="bottom">14</div>
          </div>
        </div>
        <div class="segment-title">Days</div>
      </div>
      <div class="container-segment">
        <div class="segment">
          <div class="flip-card" ref="data_hours">
            <div ref="top" class="top">24</div>
            <div ref="bottom" class="bottom">24</div>
          </div>
        </div>
        <div class="segment-title">Hours</div>
      </div>
      <div class="container-segment">
        <div class="segment">
          <div class="flip-card" ref="data_minutes">
            <div ref="top" class="top">00</div>
            <div ref="bottom" class="bottom">00</div>
          </div>
        </div>
        <div class="segment-title">Minutes</div>
      </div>
      <div class="container-segment">
        <div class="segment">
          <div class="flip-card" ref="data_seconds">
            <div ref="top" class="top">00</div>
            <div ref="bottom" class="bottom">00</div>
          </div>
        </div>
        <div class="segment-title">Seconds</div>
      </div>
    </div>
    <ul class="social">
      <li>
        <a href="https://www.facebook.com/catalinmuresiangabriel" target="_blank">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24"><path fill="#8385A9" d="M22.675 0H1.325C.593 0 0 .593 0 1.325v21.351C0 23.407.593 24 1.325 24H12.82v-9.294H9.692v-3.622h3.128V8.413c0-3.1 1.893-4.788 4.659-4.788 1.325 0 2.463.099 2.795.143v3.24l-1.918.001c-1.504 0-1.795.715-1.795 1.763v2.313h3.587l-.467 3.622h-3.12V24h6.116c.73 0 1.323-.593 1.323-1.325V1.325C24 .593 23.407 0 22.675 0z"/></svg>
        </a>
      </li>
      <li>
        <a href="https://www.pinterest.com/" target="_blank">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24"><path fill="#8385A9" d="M12 0C5.373 0 0 5.372 0 12c0 5.084 3.163 9.426 7.627 11.174-.105-.949-.2-2.405.042-3.441.218-.937 1.407-5.965 1.407-5.965s-.359-.719-.359-1.782c0-1.668.967-2.914 2.171-2.914 1.023 0 1.518.769 1.518 1.69 0 1.029-.655 2.568-.994 3.995-.283 1.194.599 2.169 1.777 2.169 2.133 0 3.772-2.249 3.772-5.495 0-2.873-2.064-4.882-5.012-4.882-3.414 0-5.418 2.561-5.418 5.207 0 1.031.397 2.138.893 2.738a.36.36 0 01.083.345l-.333 1.36c-.053.22-.174.267-.402.161-1.499-.698-2.436-2.889-2.436-4.649 0-3.785 2.75-7.262 7.929-7.262 4.163 0 7.398 2.967 7.398 6.931 0 4.136-2.607 7.464-6.227 7.464-1.216 0-2.359-.631-2.75-1.378l-.748 2.853c-.271 1.043-1.002 2.35-1.492 3.146C9.57 23.812 10.763 24 12 24c6.627 0 12-5.373 12-12 0-6.628-5.373-12-12-12z"/></svg>
        </a>
      </li>
      <li>
        <a href="https://www.instagram.com/catalinmuresian"  target="_blank">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24"><path fill="#8385A9" d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zM12 0C8.741 0 8.333.014 7.053.072 2.695.272.273 2.69.073 7.052.014 8.333 0 8.741 0 12c0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98C8.333 23.986 8.741 24 12 24c3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98C15.668.014 15.259 0 12 0zm0 5.838a6.162 6.162 0 100 12.324 6.162 6.162 0 000-12.324zM12 16a4 4 0 110-8 4 4 0 010 8zm6.406-11.845a1.44 1.44 0 100 2.881 1.44 1.44 0 000-2.881z"/></svg>
        </a>
      </li>
    </ul>
    <div class="attribution">
      Challenge by <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>.
      Coded by <a href="https://github.com/catalinmuresian">Catalin Muresian</a>.
    </div>
  </div>
</template>

<script setup>

import {ref} from "vue";

const top = ref(null)
const bottom = ref(null)

const data_days = ref(null)
const data_hours = ref(null)
const data_minutes = ref(null)
const data_seconds = ref(null)

const countToDate = new Date(Date.now() + 12096e5);

setInterval(() => {
  let now = new Date().getTime();
  let distance = countToDate - now;
  flipAllCards(distance)
}, 250)

function flipAllCards(distance) {

  const days = Math.floor(distance / (1000 * 60 * 60 * 24));
  const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
  const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
  const seconds = Math.floor((distance % (1000 * 60)) / 1000);


  flip(data_days.value, days)
  flip(data_hours.value, hours)
  flip(data_minutes.value, minutes)
  flip(data_seconds.value , seconds)
}

function flip(flipCard, newNumber) {
  const topHalf = flipCard.querySelector(".top")
  const startNumber = parseInt(topHalf.textContent)
  if (newNumber === startNumber) return

  const bottomHalf = flipCard.querySelector(".bottom")
  const topFlip = document.createElement("div")
  topFlip.classList.add("top-flip")
  const bottomFlip = document.createElement("div")
  bottomFlip.classList.add("bottom-flip")

  top.textContent = startNumber
  bottomHalf.textContent = startNumber
  topFlip.textContent = startNumber
  bottomFlip.textContent = newNumber

  topFlip.addEventListener("animationstart", e => {
    topHalf.textContent = newNumber
  })
  topFlip.addEventListener("animationend", e => {
    topFlip.remove()
  })
  bottomFlip.addEventListener("animationend", e => {
    bottomHalf.textContent = newNumber
    bottomFlip.remove()
  })
  flipCard.append(topFlip, bottomFlip)
}

</script>

<style lang="scss">
.main-page {
  display: flow-root;
  background-image: url("../assets/Desktop.png");
  height: 100vh;
  background-position: center center;
  background-size: cover;
  h1 {
    color: #FFF;
    text-align: center;
    margin-top: 132px;
    margin-bottom: 104px;
    font-size: 22px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
    letter-spacing: 7.5px;
    text-transform: uppercase;
  }
  .container {
    display: flex;
    gap: 32px;
    justify-content: center;
    .container-segment {
      display: flex;
      flex-direction: column;
      gap: .1em;
      align-items: center;
      .segment {
        display: flex;
        gap: .1em;
        .flip-card {
          position: relative;
          display: inline-flex;
          flex-direction: column;
          box-shadow: 0 10px 0 0 #191A23;
          border-radius: .1em;
          font-size: 80px;
          font-weight: 700;
          line-height: 71px;

        }

        .top,
        .bottom,
        .flip-card .top-flip,
        .flip-card .bottom-flip {
          background-color: #2C2E44;
          width: 147px;
          height: 70px;
          line-height: 1.247;
          padding: .25em;
          overflow: hidden;
          text-align: center;
        }

        .top,
        .flip-card .top-flip {
          background-color: #2C2E44;
          border-top-right-radius: 8px;
          border-top-left-radius: 8px;
          -webkit-background-clip: padding-box; /* for Safari */
          background-clip: padding-box;
          border-bottom: 0.3px solid rgba(0, 0, 0, 0.25);
          --mask: radial-gradient(6px at 40px 100%,#0000 98%,#000) -40px;
          mask: var(--mask);
          width: 147px;
          height: 70px;

        }

        .bottom,
        .flip-card .bottom-flip {
          background-color: #343650;
          display: flex;
          align-items: flex-end;
          border-bottom-right-radius: 8px;
          border-bottom-left-radius: 8px;
          --mask: radial-gradient(6px at 40px 0,#0000 98%,#000) -40px;
          mask: var(--mask);
          width: 147px;
          height: 70px;

          justify-content: center;


        }

        .flip-card .top-flip {
          position: absolute;
          width: 100%;
          animation: flip-top 250ms ease-in;
          transform-origin: bottom;
        }
        @keyframes flip-top {
          100% {
            transform: rotateX(90deg);
          }
        }

        .flip-card .bottom-flip {
          position: absolute;
          bottom: 0;
          width: 100%;
          animation: flip-bottom 250ms ease-out 250ms;
          transform-origin: top;
          transform: rotateX(90deg);
        }
        @keyframes flip-bottom {
          100% {
            transform: rotateX(0deg);
          }
        }

      }
      .segment-title {
        margin-top: 26px;
        text-transform: uppercase;
        color: #8385A9;
        text-align: center;
        font-size: 14px;
        font-style: normal;
        font-weight: 700;
        line-height: normal;
        letter-spacing: 5.919px;
      }
    }
  }
  .social {
    position: absolute;
    bottom: 48px;
    left: 0;
    right: 0;
    display: flex;
    justify-content: space-between;
    width: 136px;
    margin: 0 auto;
    list-style-type: none;
    padding: 0;
    a:hover path {
      fill: #fb6087;
    }
  }
  .attribution {
    font-size: 11px;
    text-align: center;
    color: grey;
    margin-bottom: 10px;
    margin-top: 10px;
    position: absolute;
    left: 0;
    right: 0;
    top: 10px;
    a {
      text-decoration: none;
      color: white;
    }
  }
  @media only screen and (max-width: 700px) {
    background-image: url("../assets/Mobile.png");
    .social {
      bottom: 72px;
    }
    h1 {
      font-size: 18px;
      width: 327px;
      margin: 142px auto 54px;
    }
    .segment-title {
      font-size: 7px;
      letter-spacing: 2.959px;
      margin-top: 14px;
    }
    .container {
      gap: 16px;
    }
    .flip-card {
      font-size: 36px;
      box-shadow: 0 5px 0 0 #191A23;
    }
    .top,
    .bottom,
    .flip-card .top-flip,
    .flip-card .bottom-flip {
      width: 70px;
      height: 33px;
      line-height: 1.33;
    }
    .top,
    .bottom,
    .bottom-flip
    .flip-card
    .top-flip {
      width: 70px;
      height: 33px;
    }
    .top,
    .flip-card .top-flip {
      --mask: radial-gradient(3px at 40px 100%,#0000 98%,#000) -40px;
    }
    .bottom,
    .flip-card .bottom-flip {
      --mask: radial-gradient(3px at 40px 0,#0000 98%,#000) -40px;
    }
  }
}
</style>
