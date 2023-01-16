<template>
  <section class="hello">
    <h3>Say hello to NOXICA</h3>
    <p>
      Easily setup and activate the AI. Save time with valuable inbuilt presets.
      Perfect for almost any kind of usage, digital nomads, freelancers, and
      just about everyone.
    </p>
    <img
      src="@/assets/hello.png"
      width="517"
      height="512"
      alt="A smiling camera lens"
    />
    <button>Own your own personal AI Today</button>
  </section>
</template>

<style scoped lang="scss">
.hello {
  background-color: $bg;
  padding: 3rem 8%;
  height: 100vh;
  text-align: center;
  position: relative;
  overflow: hidden;
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
