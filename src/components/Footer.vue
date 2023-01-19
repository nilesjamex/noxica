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
        src="@/assets/Ai.8dc11f79.png"
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
  @include respondMax("tablet2x") {
    flex-direction: column;
  }
  &__info {
    &__text {
      @extend %flex-ac-jb;
      padding-left: 0rem;
      margin-top: 2rem;
      margin-right: -6rem;
      @include respondMax("tablet2x") {
        flex-wrap: wrap;
        margin-right: unset;
        gap: 1.5rem;
        margin-bottom: 1.5rem;
      }
      p {
        font-family: "Neue Montreal", sans-serif;
        font-style: normal;
        font-weight: 500;
        font-size: Max(1rem, 16px);
        line-height: Max(1.195rem, 19px);
        color: $white;
        height: auto;
        &.list {
          @extend %flex-ac;
          gap: 1rem;
          @include respondMax("tablet2x") {
            flex-wrap: wrap;
          }
        }
      }
    }
  }
  &__links {
    @extend %flex-ac-jb;
    @include respondMax("tablet2x") {
      flex-wrap: wrap;
      gap: 1.5rem;
    }
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
    @include respondMax("tablet2x") {
      flex-wrap: wrap;
      margin-right: unset;
      img {
        width: 100%;
        object-fit: contain;
      }
    }
    .icons {
      @extend %center;
      gap: 1rem;
      margin: 0 0 0 3rem;
      img {
        cursor: pointer;
      }
    }
  }
}
</style>
