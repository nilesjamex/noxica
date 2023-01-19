<template>
  <section class="hero">
    <nav class="hero__nav">
      <p>noxica.</p>
      <div
        class="hero__nav__items"
        :class="{ hero__nav__items__active: active }"
      >
        <p @click="active = !active">Resources</p>
        <p @click="active = !active">Support</p>
        <p @click="active = !active">Company</p>
        <p @click="active = !active">Partners</p>
        <button @click="active = !active">Get Started</button>
      </div>
      <div class="toggle" @click="active = !active">
        <div class="box"></div>
        <div class="box"></div>
        <div class="box"></div>
      </div>
    </nav>
    <div class="hero__content">
      <div class="item">
        <h2
          data-aos="fade-up"
          data-aos-duration="500"
          data-aos-easing="ease-in-back"
          data-aos-delay="100"
        >
          AI Powered <br />
          Virtual Personal Assistants.
        </h2>
        <p
          data-aos="fade-up"
          data-aos-duration="500"
          data-aos-easing="ease-in-back"
          data-aos-delay="200"
        >
          Save time, money, effort, use our feature-loaded AI personal virtual
          assistants for personal and business users.
        </p>
        <button
          data-aos="fade-up"
          data-aos-duration="500"
          data-aos-delay="300"
          data-aos-anchor-placement="center-bottom"
        >
          Get Started
        </button>
      </div>
    </div>
  </section>
</template>

<script setup>
import { onMounted, ref } from "vue";
import AOS from "aos";
import "aos/dist/aos.css";
onMounted(() => {
  AOS.init();
});
const active = ref(false);
</script>

<style scoped lang="scss">
.hero {
  background-color: $bg;
  padding: 3rem 8%;
  height: 100vh;
  text-align: center;
  position: relative;
  background-image: url("@/assets/bg1.png");
  background-repeat: no-repeat;
  background-size: contain;
  z-index: 3;
  @include respondMax("tablet2x") {
    height: auto;
    background-image: unset;
  }
  &::before {
    content: "";
    position: absolute;
    z-index: -1;
    height: 100vh;
    width: 100vw;
    top: 0;
    right: 0;
    background-image: url("@/assets/bg2.png");
    background-repeat: no-repeat;
    background-size: contain;
    background-position: 100% center;
    @include respondMax("tablet2x") {
      height: auto;
    }
  }
  &__nav {
    @extend %flex-ac-jb;
    padding: 0.5rem 2rem;
    @include respondMax("tablet2x") {
      margin-bottom: 3rem;
    }
    p {
      font-family: "Neue Montreal", sans-serif;
      font-style: normal;
      font-weight: 400;
      font-size: Max(1.25rem, 20px);
      line-height: Max(1.5rem, 24px);
      text-align: center;
      color: $white;
    }
    .toggle {
      display: none;
      @include respondMax("tablet2x") {
        display: block;
        z-index: 3;
      }
      .box {
        width: 25px;
        height: 1.5px;
        background-color: $green;
        margin: 0.25rem 0;
      }
    }
    &__items {
      @extend %flex-ac;
      gap: 1.5rem;
      @include respondMax("tablet2x") {
        position: fixed;
        display: flex;
        flex-direction: column;
        gap: 1.5rem;
        top: 8vh;
        bottom: 0;
        right: 0;
        order: 1;
        transition: all 0.2s ease-out;
        overflow: hidden;
        z-index: 2;
        padding: 5% 1.5rem 3%;
        height: 100%;
        width: 100%;
        background-color: $bg;
        transform: translateX(100%);
        &__active {
          transform: translateX(0%);
        }
      }
      p {
        font-family: "Neue Montreal", sans-serif;
        font-style: normal;
        font-weight: 400;
        font-size: Max(1rem, 16px);
        line-height: Max(1.195rem, 19px);
        color: $white;
        position: relative;
        cursor: pointer;
        &::after {
          transition: all ease-in-out 0.7s;
          position: absolute;
          width: 0%;
          content: "";
          left: 0;
          bottom: 0;
          height: 2px;
          background: $green;
        }
        &:hover {
          &::after {
            width: 100%;
          }
        }
      }
      button {
        font-family: "Neue Montreal", sans-serif;
        font-style: normal;
        font-weight: 400;
        font-size: Max(1rem, 16px);
        line-height: Max(1.195rem, 19px);
        color: $white;
        border: 1px solid #00af7e;
        background-color: transparent;
        padding: 10px;
        width: Max(13.8125rem, 221px);
        height: Max(3.75rem, 60px);
        transition: all 0.6s ease-in-out;
        cursor: pointer;
        &:hover {
          background-color: $green;
          color: $white;
          transition: all 0.6s ease-in-out;
        }
      }
    }
  }
  &__content {
    height: 90%;
    @extend %center;
    h2 {
      font-family: "Neue Montreal", sans-serif;
      font-style: normal;
      font-weight: 400;
      font-size: Max(6.25rem, 40px);
      line-height: Max(7.5rem, 50px);
      text-align: center;
      color: $white;
      @include respondMax("tablet2x") {
        font-size: Max(3rem, 24px);
        line-height: 120%;
      }
    }
    p {
      font-family: "Neue Montreal", sans-serif;
      font-style: normal;
      font-weight: 400;
      font-size: Max(1.25rem, 20px);
      line-height: Max(1.5rem, 24px);
      text-align: center;
      color: $white;
    }
    button {
      font-family: "Neue Montreal", sans-serif;
      font-style: normal;
      font-weight: 400;
      font-size: Max(1rem, 16px);
      line-height: Max(1.195rem, 19px);
      color: $white;
      border: 1px solid #00af7e;
      background-color: $green;
      padding: 10px;
      width: Max(13.8125rem, 221px);
      height: Max(3.75rem, 60px);
      transition: all 0.1s ease-in-out;
      cursor: pointer;
      margin-top: 1.5rem;
    }
  }
}
</style>
