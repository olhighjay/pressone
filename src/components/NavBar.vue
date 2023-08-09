<template>
  <div :class="['w-100 nav-cover', { 'window-scrolled': isScrolling }]">
    <!-- large screen navigation bar start -->
    <nav class="d-flex nav header-container max-container">
      <div class="nav-logo-cover">
        <img alt="Press One Africa" src="../assets/images/svg/logo.svg" />
      </div>
      <div class="d-flex w-100 lg-nav">
        <ul class="nav-list">
          <li class="nav-list-item">About Us</li>
          <li class="nav-list-item">Pricing</li>
          <li class="nav-list-item">product</li>
          <li class="nav-list-item">Support</li>
        </ul>
        <div class="nav-btn-cover">
          <button class="btn text-primary nav-btn">Get PressOne</button>
        </div>
      </div>
      <!-- mobile sidebar cta -->
      <div class="md-nav-harmburger-cover w-100 text-right">
        <img
          v-if="!showMobileSidebar"
          @click="showMobileSidebar = true"
          alt="Open Sidebar"
          src="../assets/images/svg/harmburger-menu.svg"
        />
        <img
          v-else
          @click="showMobileSidebar = false"
          alt="Close Sidebar"
          src="../assets/images/svg/close-menu.svg"
        />
      </div>
    </nav>
    <!-- large screen navigation bar end -->

    <!-- Mobile sidebar start-->
    <transition name="sidebar-fade" mode="out-in" appear>
      <aside v-if="showMobileSidebar" class="mobile-aside">
        <ul class="mobile-aside-list">
          <li class="nav-list-item mobile-aside-list-item">About Us</li>
          <li class="nav-list-item mobile-aside-list-item">Pricing</li>
          <li class="nav-list-item mobile-aside-list-item">product</li>
          <li class="nav-list-item mobile-aside-list-item">Support</li>
        </ul>

        <div class="pl-40 text-primary">Get PressOne</div>
      </aside>
    </transition>
    <!-- Mobile sidebar end -->
  </div>
</template>

<script setup>
import { ref, onMounted, onBeforeMount } from "vue";

const currentScrollPosition = ref(0);
const isScrolling = ref(false);
const showMobileSidebar = ref(false);

const onScroll = () => {
  currentScrollPosition.value =
    window.pageYOffset || document.documentElement.scrollTop;

  isScrolling.value = currentScrollPosition.value > 2 ? true : false;
};

onMounted(() => {
  window.addEventListener("scroll", onScroll);
});

onBeforeMount(() => {
  window.removeEventListener("scroll", onScroll);
});
</script>

<style scoped lang="scss">
$basic-color: #0e99d2;

.nav-cover {
  position: fixed;
  top: 0;
  left: 0;
  z-index: 10000;

  &.window-scrolled {
    background: #ffff;
    box-shadow: rgba(0, 0, 0, 0.15) 1.95px 1.95px 2.6px;
  }
}
.nav {
  font-size: 18px;
  font-style: normal;
  font-weight: 500;
  line-height: 140%;

  .lg-nav {
    @media screen and (max-width: 1000px) {
      display: none;
    }
  }

  &-logo-cover {
    flex-basis: 25%;
    padding-top: 8px;
  }

  &-list {
    list-style: none;
    display: inline-flex;
    gap: 50px;
    margin-right: auto;

    &-item {
      cursor: pointer;

      &:hover {
        color: $basic-color;
      }
    }
  }

  &-btn-cover {
    padding-top: 3px;
  }

  &-btn {
    border-radius: 4px;
    border: 1px solid $basic-color;
    background: transparent;
    padding: 14px 24px;
  }
}

.sidebar-fade-enter-active,
.sidebar-fade-leave-active {
  transition: transform 0.2s ease;
}

.sidebar-fade-enter,
.sidebar-fade-leave-to {
  transform: translateY(-200%);
  transition: all 300ms ease-in 0s;
}

.md-nav-harmburger-cover {
  display: none;

  @media screen and (max-width: 1000px) {
    display: block;
  }
}

.mobile-aside {
  position: fixed;
  top: 70px;
  right: 0;
  z-index: 100;
  background: #fff;
  width: 100vw;
  box-shadow: 1px 1px 1px 0 #0000002e;
  padding: 10px 0 50px 0;

  &-list {
    list-style: none;

    &-item {
      line-height: 45px;
    }
  }
}
</style>
