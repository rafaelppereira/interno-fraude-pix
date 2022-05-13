<template>
  <div class="clock">
    <div class="title">
      <h2>Falta <span>pouco tempo</span> para o <span>lançamento</span></h2>
      <p>Estamos implementando as funcionalidades para trazer o <span>Pix Seguro</span> para você</p>
    </div>
    <div class="countdown">
      <div class="countdownContainer">
        <div>
          <span>{{ days }}</span>
        </div>
        <span>:</span>
        <div>
          <span>{{ hours }}</span>
        </div>
        <span>:</span>
        <div>
          <span>{{ minutes }}</span>
        </div>
        <span>:</span>
        <div>
          <span>{{ seconds }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'ClockItem',
  data () {
    return {
      days: null,
      hours: null,
      minutes: null,
      seconds: null
    }
  },
  mounted () {
    setInterval(() => {
      this.getDays()
      this.getHours()
      this.getMinutes()
      this.getSeconds()
    }, 1000)
  },
  methods: {
    getDays () {
      const nextYear = new Date().getFullYear() + 1
      const newYearTime = new Date(`January 01 ${nextYear} 00:00:00`)

      const currentTime = new Date()
      const difference = newYearTime - currentTime
      const days = Math.floor(difference / 1000 / 60 / 60 / 24)

      return this.days = days
    },
    getHours () {
      const nextYear = new Date().getFullYear() + 1
      const newYearTime = new Date(`January 01 ${nextYear} 00:00:00`)

      const currentTime = new Date()
      const difference = newYearTime - currentTime
      const hours = Math.floor(difference / 1000 / 60 / 60) % 24

      return this.hours = hours
    },
    getMinutes () {
      const nextYear = new Date().getFullYear() + 1
      const newYearTime = new Date(`January 01 ${nextYear} 00:00:00`)

      const currentTime = new Date()
      const difference = newYearTime - currentTime
      const minutes = Math.floor(difference / 1000 / 60) % 60

      return this.minutes = minutes
    },
    getSeconds () {
      const nextYear = new Date().getFullYear() + 1
      const newYearTime = new Date(`January 01 ${nextYear} 00:00:00`)

      const currentTime = new Date()
      const difference = newYearTime - currentTime
      const seconds = Math.floor(difference / 1000) % 60

      return this.seconds = seconds
    }
  }
}
</script>

<style lang="scss">
  .clock {
    padding: 6rem 0 4rem 0;

    .title {
      text-align: center;

      h2 {
        font-size: 2rem;
        font-weight: 500;
        color: #ffffff;

        span {
          color: #009B90;
          font-weight: 600;
        }
      }

      p {
        color: #ffffff;
        opacity: 0.6;
        font-weight: 300;
      }
    }

    .countdown {

      .countdownContainer {
        display: flex;
        align-items: center;
        font-family: Rajdhani;
        font-weight: 600;
        color: #181818;

        width: 100%;

        margin-top: 5rem;

        @media (max-width: 650px) {
          flex-direction: column;
        }

        > div {
          flex: 1;
          display: flex;
          justify-content: space-evenly;
          align-items: center;
          padding: 0 1rem;

          background: #ffffff;
          box-shadow: 0 0 60px rgba(0,0,0,0.5);
          border-radius: 5px;
          font-size: 8rem;
          text-align: center;

          @media (max-width: 768px) {
            font-size: 7rem;
          }

          span {
            flex: 1;

            &:first-child {
              border-right: 1px solid #f0f1f3;
              padding: 0 1rem;
            }

            &:last-child {
              border-left: 1px solid #f0f1f3;
              padding: 0 1rem;
            }
          }
        }

        > span {
          font-size: 6.25rem;
          margin: 0 0.5rem;
          color: #ffffff;
        }
      }
    }
  }
</style>
