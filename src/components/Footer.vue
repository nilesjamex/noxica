<template>
  <section class="footer">
    <div class="footer__info">
      <div class="footer__links">
        <dl>
          <dt>Company</dt>
          <dd v-for="item in footer" :key="item.id">
            {{ item.item }}
          </dd>
        </dl>
        <dl>
          <dt>Company</dt>
          <dd v-for="item in footer" :key="item.id">
            {{ item.item }}
          </dd>
        </dl>
        <dl>
          <dt>Company</dt>
          <dd v-for="item in footer" :key="item.id">
            {{ item.item }}
          </dd>
        </dl>
        <dl>
          <dt>Company</dt>
          <dd v-for="item in footer" :key="item.id">
            {{ item.item }}
          </dd>
        </dl>
      </div>
      <div class="footer__info__text">
        <p>AI‑Powered Secured Chain Protocol, 2023.</p>
        <p class="list">
          <span>Privacy Policy</span><span>Cookie Policy</span
          ><span>User Agreement</span><span>Terms and Condition</span>
        </p>
      </div>
    </div>
    <div class="footer__socials">
      <div class="icons">
        <img src="@/assets/insta.svg" alt="instagram" width="24" height="24" />
        <img src="@/assets/github.svg" alt="github" width="24" height="24" />
        <img src="@/assets/discord.svg" alt="discord" width="24" height="24" />
        <img src="@/assets/twitter.svg" alt="twitter" width="24" height="24" />
        <img src="@/assets/reddit.svg" alt="reddit" width="24" height="24" />
      </div>
      <img
        src="@/assets/Ai.png"
        alt="an image of a robot"
        width="560"
        height="309"
        class="robot"
      />
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";

const footer = ref([
  {
    id: 2,
    item: "About us",
  },
  {
    id: 3,
    item: "Partners",
  },
  {
    id: 4,
    item: "Overview",
  },
  {
    id: 5,
    item: "Security",
  },
]);
</script>

<style scoped lang="scss">
.footer {
  background-color: $bg;
  padding: 3rem 8% 0;
  @extend %flex-ac-jb;
  overflow: hidden;
  &__info {
    &__text {
      @extend %flex-ac-jb;
      padding-left: 3rem;
      margin-top: 2rem;
      margin-right: -6rem;
      p {
        font-family: "Neue Montreal", sans-serif;
        font-style: normal;
        font-weight: 500;
        font-size: Max(1rem, 16px);
        line-height: Max(1.195rem, 19px);
        color: $white;
        &.list {
          @extend %flex-ac;
          gap: 1rem;
        }
      }
    }
  }
  &__links {
    @extend %flex-ac-jb;
    dl {
      dt {
        font-family: "Neue Montreal", sans-serif;
        font-style: normal;
        font-weight: 500;
        font-size: Max(1rem, 16px);
        line-height: Max(1.195rem, 19px);
        color: $white;
        margin-bottom: 1rem;
      }
      dd {
        font-family: "Neue Montreal", sans-serif;
        font-style: normal;
        font-weight: 100;
        font-size: Max(1rem, 16px);
        line-height: Max(1.563rem, 25px);
        color: $white;
        margin-bottom: 0.5rem;
      }
    }
  }
  &__socials {
    margin-right: -10rem;
    .icons {
      @extend %center;
      gap: 1rem;
      margin: 0 0 0 3rem;
    }
  }
}
</style>
