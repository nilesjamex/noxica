<template>
  <section class="testimonial">
    <div class="testimonial__content">
      <div class="testimonial__text">
        <h2
          data-aos="fade-up"
          data-aos-duration="1000"
          data-aos-easing="linear"
          data-aos-delay="100"
        >
          Since 2023, Noxica has helped people throughout the world manage their
          daily lives in the most natural way possible.
        </h2>
        <p data-aos="fade-up" data-aos-duration="1700" data-aos-easing="linear">
          There will be no queuing for guidance and support or verification, no
          arbitration clause, no hidden costs, and no nonsense.
        </p>
        <button
          data-aos="fade-up"
          data-aos-duration="2000"
          data-aos-easing="linear"
          data-aos-delay="300"
          data-aos-anchor-placement="center-bottom"
        >
          Start using NOXICA today.
        </button>
      </div>
      <div class="testimonial__grid">
        <div class="item">
          <div class="item__intro">
            <img
              src="@/assets/pfp3.png"
              alt="profile picture"
              width="48"
              height="48"
            />
            <span>
              <h6>Omah Lay</h6>
              <p>Soul Singer</p>
            </span>
          </div>
          <p>
            This has literally took my pain away! I do not feel all left alone
            anymore, the AI features are insane, i had to give it a name, i
            named it “SOSO” The overall service is great and highly recommend.
          </p>
        </div>
        <div class="item item__arrow">
          <img
            src="@/assets/arr-right.svg"
            alt="a right arrow"
            width="72"
            height="72"
          />
          <img
            src="@/assets/arr-left.svg"
            alt="a left arrow"
            width="72"
            height="72"
          />
        </div>
        <div class="item">
          <div class="item__intro">
            <img
              src="@/assets/pfp1.png"
              alt="profile picture"
              width="48"
              height="48"
            />
            <span>
              <h6>Portable Omolalomi</h6>
              <p>Wahala Singer</p>
            </span>
          </div>
          <p>
            This has literally took my pain away! I do not feel all left alone
            anymore, the AI features are insane, i had to give it a name, i
            named it “SOSO” The overall service is great and highly recommend.
          </p>
        </div>
        <div class="item">
          <div class="item__intro">
            <img
              src="@/assets/pfp4.png"
              alt="profile picture"
              width="48"
              height="48"
            />
            <span>
              <h6>Omah Lay</h6>
              <p>Soul Singer</p>
            </span>
          </div>
          <p>
            This has literally took my pain away! I do not feel all left alone
            anymore, the AI features are insane, i had to give it a name, i
            named it “SOSO” The overall service is great and highly recommend.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { onMounted } from "vue";
import AOS from "aos";
import "aos/dist/aos.css";
onMounted(() => {
  AOS.init();
});
</script>

<style lang="scss" scoped>
.testimonial {
  background-color: $bg;
  padding: 3rem 8%;
  height: 100vh;
  position: relative;
  @extend %center;
  &__content {
    @include flex(flex-start, space-between, row nowrap);
    gap: 2rem;
  }
  &__text {
    h2 {
      font-family: "Neue Montreal";
      font-style: normal;
      font-weight: 400;
      font-size: Max(3rem, 24px);
      line-height: Max(3.625rem, 58px);
      color: $white;
    }
    p {
      font-family: "Neue Montreal", sans-serif;
      font-style: normal;
      font-weight: 400;
      font-size: Max(1.25rem, 20px);
      line-height: Max(1.5rem, 24px);
      color: $white;
      margin-top: 2.5rem;
    }
    button {
      background-color: $green;
      padding: 10px;
      width: Max(13.8125rem, 221px);
      height: Max(3.75rem, 60px);
      font-family: "Neue Montreal", sans-serif;
      font-style: normal;
      font-weight: 400;
      font-size: Max(1rem, 16px);
      line-height: Max(1.195rem, 19px);
      color: $white;
      margin-top: 2rem;
    }
  }
  &__grid {
    display: grid;
    grid-template-columns: 299px 280px;
    grid-template-rows: 250px 260px;
    gap: 1.5rem;
    .item {
      background-color: transparent;
      background-image: url("@/assets/Union-bg.png");
      background-repeat: no-repeat;
      background-size: cover;
      width: 299.25px;
      height: 224.32px;
      filter: drop-shadow(0px 4px 20px rgba(0, 0, 0, 0.1));
      padding: 1.25rem 0.8rem;
      &:nth-child(1) {
        margin-left: 2rem;
        &:hover {
          animation-name: bounce-6;
          animation-timing-function: ease;
          animation-duration: 2s;
          animation-iteration-count: infinite;
        }
      }
      &:nth-child(4) {
        margin-top: -2rem;
        margin-left: 1rem;
        &:hover {
          animation-name: bounce-6;
          animation-timing-function: ease;
          animation-duration: 2s;
          animation-iteration-count: infinite;
        }
      }
      &:nth-child(3) {
        &:hover {
          animation-name: bounce-6;
          animation-timing-function: linear;
          animation-duration: 2s;
          animation-iteration-count: infinite;
        }
      }
      &__arrow {
        @extend %center;
        gap: 1rem;
        background-image: none;
      }
      &__intro {
        @extend %flex-ac;
        gap: 0.75rem;
        margin-bottom: 1rem;
        h6 {
          font-family: "Neue Montreal", sans-serif;
          font-style: normal;
          font-weight: 400;
          font-size: Max(1rem, 16px);
          line-height: Max(1.195rem, 19px);
          color: $white;
          margin-top: 0.3rem;
        }
        p {
          font-family: "Neue Montreal", sans-serif;
          font-style: normal;
          font-weight: 400;
          font-size: Max(0.75rem, 12px);
          line-height: Max(0.875rem, 14px);
          color: $white;
        }
      }
      p {
        font-family: "Neue Montreal", sans-serif;
        font-style: normal;
        font-weight: 400;
        font-size: Max(1rem, 16px);
        line-height: Max(1.25rem, 20px);
        color: $white;
      }
    }
  }
  @keyframes bounce-6 {
    0% {
      transform: scale(1, 1) translateY(0);
    }
    10% {
      transform: scale(1.1, 0.9) translateY(0);
    }
    30% {
      transform: scale(0.9, 1.1) translateY(-100px);
    }
    50% {
      transform: scale(1.05, 0.95) translateY(0);
    }
    57% {
      transform: scale(1, 1) translateY(-7px);
    }
    64% {
      transform: scale(1, 1) translateY(0);
    }
    100% {
      transform: scale(1, 1) translateY(0);
    }
  }
}
</style>
