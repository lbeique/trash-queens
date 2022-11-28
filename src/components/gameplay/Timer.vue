
<template>
  <div>
    <div class="base-timer">
      <svg class="base-timer__svg" viewBox="0 0 100 100">
        <g class="base-timer__circle">
          <circle class="base-timer__path-elapsed" cx="50" cy="50" r="45" />
          <path id="base-timer-path-remaining" stroke-dasharray="283" class="base-timer__path-remaining" d="
          M 50, 50
          m -45, 0
          a 45,45 0 1,0 90,0
          a 45,45 0 1,0 -90,0
        "></path>
        </g>
      </svg>
      <span id="base-timer-label" class="base-timer__label">
        <!-- Remaining time label -->
        {{ startTimer() }}
      </span>
    </div>
  </div>
</template>


<script>
export default {
  props: {
    "finalScore": INTEGER
  },
  data() {
    return {
      TIME_LIMIT: 5,
      timePassed: 0,
      timeLeft: this.TIME_LIMIT,
      timerInterval: null,
      FULL_DASH_ARRAY: 283
    }
  },
  computed: {
    goToResults() {
      this.$router.push({ path: `/result/${this.finalScore}` })
    }
  },
  methods: {
    startTimer() {
      this.timerInterval = setInterval(() => {

        if (this.timeLeft == 0) {
          goToResults()
          // this.timePassed = 0;
        } else {
          // The amount of time passed increments by one
          this.timePassed = this.timePassed += 1;
        }

        this.timeLeft = this.TIME_LIMIT - this.timePassed;

        // The time left label is updated
        document.getElementById("base-timer-label").innerHTML = this.timeLeft;
        // this.setCircleDasharray();
      }, 1000)
    }
  },
  // Divides time left by the defined time limit.
  calculateTimeFraction() {
    const rawTimeFraction = timeLeft / TIME_LIMIT;
    return rawTimeFraction - (1 / TIME_LIMIT) * (1 - rawTimeFraction);
  },

  // Update the dasharray value as time passes, starting with 283
  setCircleDasharray() {
    const circleDasharray = `${(
      calculateTimeFraction() * FULL_DASH_ARRAY
    ).toFixed(0)} 283`;
    document
      .getElementById("base-timer-path-remaining")
      .setAttribute("stroke-dasharray", circleDasharray);
  }
};
</script>


<style scoped>
.base-timer {
  position: relative;
  height: 30vw;
  width: 30vw;
}

/* Removes SVG styling that would hide the time label */
.base-timer__circle {
  /* fill: none; */
  fill: #ffdc7d74;
  stroke: none;
}

/* The SVG path that displays the timer's progress */
.base-timer__path-elapsed {
  stroke-width: 10%;
  stroke: #D8C590;
}

.base-timer__label {
  position: absolute;

  /* Size should match the parent container */
  width: 30vw;
  height: 30vw;

  /* Keep the label aligned to the top */
  top: 0;

  /* Create a flexible box that centers content vertically and horizontally */
  display: flex;
  align-items: center;
  justify-content: center;

  /* Sort of an arbitrary number; adjust to your liking */
  font-size: 3rem;
  font-weight: 600;
  font-family: "Nunito-Bold", sans-serif;
  line-height: 0;
}

.base-timer__path-remaining {
  /* Just as thick as the original ring */
  stroke-width: 10%;

  /* Rounds the line endings to create a seamless circle */
  stroke-linecap: round;

  /* Makes sure the animation starts at the top of the circle */
  transform: rotate(90deg);
  transform-origin: center;

  /* One second aligns with the speed of the countdown timer */
  transition: 1s linear all;

  /* Allows the ring to change color when the color value updates */
  stroke: #5AB4AB;
}

.base-timer__svg {
  /* Flips the svg and makes the animation to move left-to-right */
  transform: scaleX(-1);
}
</style>