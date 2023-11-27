<template>
  <div class="main-page">
    <h1>We’re launching soon</h1>
    <div class="container">
      <div class="container-segment">
        <div class="segment">
          <div class="flip-card" ref="data_days">
            <div ref="top" class="top">08</div>
            <div ref="bottom" class="bottom">08</div>
          </div>
        </div>
        <div class="segment-title">Days</div>
      </div>
      <div class="container-segment">
        <div class="segment">
          <div class="flip-card" ref="data_hours">
            <div ref="top" class="top">23</div>
            <div ref="bottom" class="bottom">23</div>
          </div>
        </div>
        <div class="segment-title">Hours</div>
      </div>
      <div class="container-segment">
        <div class="segment">
          <div class="flip-card" ref="data_minutes">
            <div ref="top" class="top">55</div>
            <div ref="bottom" class="bottom">55</div>
          </div>
        </div>
        <div class="segment-title">Minutes</div>
      </div>
      <div class="container-segment">
        <div class="segment">
          <div class="flip-card" ref="data_seconds">
            <div ref="top" class="top">41</div>
            <div ref="bottom" class="bottom">41</div>
          </div>
        </div>
        <div class="segment-title">Seconds</div>
      </div>
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
}








.flip-card {
  position: relative;
  display: inline-flex;
  flex-direction: column;
  box-shadow: 0 10px 0 0 #191A23;
  border-radius: .1em;
  font-size: 92px;
}

.top,
.bottom,
.flip-card .top-flip,
.flip-card .bottom-flip {
  background-color: #2C2E44;
  height: .75em;
  line-height: 1;
  padding: .25em;
  overflow: hidden;
}

.top,
.flip-card .top-flip {
  background-color: #2C2E44;
  border-top-right-radius: 8px;
  border-top-left-radius: 8px;
 border-bottom: 0.3px solid rgba(0, 0, 0, 0.25);
  --mask: radial-gradient(6px at 40px 100%,#0000 98%,#000) -40px;
  mask: var(--mask);
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

.container {
  display: flex;
  gap: 32px;
  justify-content: center;
}

.container-segment {
  display: flex;
  flex-direction: column;
  gap: .1em;
  align-items: center;
}

.segment {
  display: flex;
  gap: .1em;
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

</style>
