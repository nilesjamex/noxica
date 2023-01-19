<template>
  <section class="hello">
    <h3
      data-aos="fade-left"
      data-aos-anchor-placement="top-bottom"
      data-aos-easing="ease-out-cubic"
      data-aos-duration="800"
    >
      Say hello to NOXICA
    </h3>
    <p
      data-aos="fade-left"
      data-aos-anchor-placement="top-bottom"
      data-aos-easing="ease-out-cubic"
      data-aos-duration="800"
    >
      Easily setup and activate the AI. Save time with valuable inbuilt presets.
      Perfect for almost any kind of usage, digital nomads, freelancers, and
      just about everyone.
    </p>
    <img
      src="@/assets/hello.png"
      width="517"
      height="512"
      alt="A smiling camera lens"
      data-aos="fade-up"
      data-aos-duration="800"
    />
    <button>Own your own personal AI Today</button>
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

<style scoped lang="scss">
.hello {
  background-color: $bg;
  padding: 3rem 8%;
  height: 100vh;
  text-align: center;
  position: relative;
  overflow: hidden;
  @include respondMax("tablet2x") {
    height: auto;
    background-image: unset;
  }
  &::before {
    content: "";
    position: absolute;
    width: 534px;
    height: 534px;
    top: 30%;
    left: -20%;
    background: #264c44;
    filter: blur(100px);
    border-radius: 30%;
    @include respondMax("tablet2x") {
      background: none;
    }
  }
  &::after {
    content: "";
    position: absolute;
    width: 534px;
    height: 434px;
    top: 10%;
    right: -20%;
    background: #a4be7b;
    filter: blur(100px);
    border-radius: 30%;
    @include respondMax("tablet2x") {
      background: none;
    }
  }
  h3 {
    font-family: "Neue Montreal", sans-serif;
    font-style: normal;
    font-weight: 400;
    font-size: Max(5rem, 40px);
    line-height: Max(6rem, 56px);
    text-align: center;
    color: $white;
  }
  p {
    font-family: "Neue Montreal", sans-serif;
    font-style: normal;
    font-weight: 400;
    font-size: Max(1.25rem, 20px);
    line-height: Max(1.5rem, 24px);
    text-align: center;
    color: $white;
    width: Min(749px, 100%);
    margin: 0.5rem auto;
  }
  img {
    margin: 0.3rem auto;
    @extend %center;
    object-fit: contain;
    @include respondMax("mobile3x") {
      width: 100%;
    }
  }
  button {
    width: Min(331px, 100%);
    height: Max(3.75rem, 60px);
    background-color: transparent;
    border: 1px solid $white;
    font-family: "Neue Montreal", sans-serif;
    font-style: normal;
    font-weight: 400;
    font-size: Max(1rem, 16px);
    line-height: Max(1.195rem, 19px);
    color: $white;
  }
}
</style>
