<template>
  <main>
    <!-- more info start -->
    <section class="bg-primary more">
      <div class="more-info d-flex header-container max-container">
        <div class="more-info-item d-flex position-relative">
          <div
            class="more-info-item-icon-wrapper d-flex flex-content-center w-100 position-absolute"
          >
            <div class="more-info-item-icon-cover">
              <img
                class="more-info-item-icon"
                src="../assets/images/svg/users.svg"
              />
            </div>
          </div>

          <p class="text-center">
            75% of consumers prefer human interactions to automated
            interactions.
          </p>
        </div>

        <div class="more-info-item position-relative">
          <div
            class="more-info-item-icon-wrapper d-flex flex-content-center w-100 position-absolute"
          >
            <div class="more-info-item-icon-cover">
              <img
                class="more-info-item-icon"
                src="../assets/images/svg/users.svg"
              />
            </div>
          </div>

          <p class="text-center">
            81% of consumers say a positive customer service experience
            increases the chances of them making another purchase.
          </p>
        </div>

        <div class="more-info-item position-relative">
          <div
            class="more-info-item-icon-wrapper d-flex flex-content-center w-100 position-absolute"
          >
            <div class="more-info-item-icon-cover">
              <img
                class="more-info-item-icon"
                src="../assets/images/svg/users.svg"
              />
            </div>
          </div>

          <p class="text-center">
            76% of surveyed customers contact customer service over the phone.
          </p>
        </div>

        <div class="more-info-item position-relative">
          <div
            class="more-info-item-icon-wrapper d-flex flex-content-center w-100 position-absolute"
          >
            <div class="more-info-item-icon-cover">
              <img
                class="more-info-item-icon"
                src="../assets/images/svg/users.svg"
              />
            </div>
          </div>

          <p class="text-center">
            68% of buyers will pay more for products and services from a company
            with a strong record of good customer service.
          </p>
        </div>
      </div>
    </section>
    <!-- more info end -->

    <!-- services start -->
    <section class="services max-container">
      <h3 class="text-center">What you get</h3>
      <div class="d-flex services-inner flex-content-center mt-60 gap-5">
        <!-- left service -->
        <div class="services-item-inner services-item">
          <div class="services-item-top services-item-top-1"></div>
          <div class="services-item-bottom position-relative">
            <div
              class="services-item-bottom-icon-wrapper d-flex flex-content-center w-100 position-absolute"
            >
              <div class="services-item-bottom-icon-cover">
                <img src="../assets/images/svg/services-1.svg" />
              </div>
            </div>
            <div class="services-item-bottom-text">
              <h3 class="text-center">Sales Support</h3>
              <!-- <ul class="mt--10"> -->
              <div class="d-flex mt--10 gap-p-15">
                <div class="pt-20">
                  <img src="../assets/images/svg/li-services-1.svg" />
                </div>
                <p>
                  We handle your enquiries, orders, reservations and help
                  improve your customers' experience.
                </p>
              </div>
              <div class="d-flex mt--10 gap-p-15">
                <div class="pt-20">
                  <img src="../assets/images/svg/li-services-1.svg" />
                </div>
                <p>
                  We send a weekly report of custom sales through a personalized
                  dashboard for your business.
                </p>
              </div>
              <div class="d-flex mt--10 gap-p-15">
                <div class="pt-20">
                  <img src="../assets/images/svg/li-services-1.svg" />
                </div>
                <p>
                  You can monitor the calls, hear the conversations and make
                  instant decisions that would grow your business at a glance.
                </p>
              </div>
              <!-- </ul> -->
            </div>
          </div>
        </div>
        <!-- right service -->
        <div class="services-item-inner services-item">
          <div class="services-item-top services-item-top-2"></div>
          <div class="services-item-bottom position-relative">
            <div
              class="services-item-bottom-icon-wrapper d-flex flex-content-center w-100 position-absolute"
            >
              <div class="services-item-bottom-icon-cover">
                <img src="../assets/images/svg/services-2.svg" />
              </div>
            </div>
            <div class="services-item-bottom-text">
              <h3 class="text-center">Customer Support</h3>
              <!-- <ul class="mt--10"> -->
              <div class="d-flex mt--10 gap-p-15">
                <div class="pt-20">
                  <img src="../assets/images/svg/li-services-2.svg" />
                </div>
                <p>
                  We handle all your customer calls and help them transition
                  through each phase of their customer journey.
                </p>
              </div>
              <div class="d-flex mt--10 gap-p-15">
                <div class="pt-20">
                  <img src="../assets/images/svg/li-services-2.svg" />
                </div>
                <p>
                  We send a weekly report of customer engagement through a
                  personalized dashboard for your business.
                </p>
              </div>
              <div class="d-flex mt--10 gap-p-15">
                <div class="pt-20">
                  <img src="../assets/images/svg/li-services-2.svg" />
                </div>
                <p>
                  You can monitor the calls, hear the conversations and make
                  instant decisions that would grow your business at a glance.
                </p>
              </div>
              <!-- </ul> -->
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- services end -->

    <!-- plans start -->
    <section class="mt-80 pt-60 max-container plans-container">
      <div class="header-container">
        <h3 class="text-center">Choose a plan that works for you</h3>
        <div class="plans d-flex flex-content-center gap-p-25 mt-40">
          <div class="plans-logo text-center">
            <img src="../assets/images/svg/plan-logo.svg" />
          </div>
          <div
            v-for="plan in plans"
            :key="plan.id"
            class="plans-item plans-item-plan"
          >
            <p class="fw-700 text-primary">{{ plan.name }}</p>
            <div>
              <span class="h3">{{ formatPrice(plan.amount) }}</span>
              <span class="text-fade">/month</span>
            </div>
            <p>{{ plan.description }}</p>
            <div class="plans-item-plan-info-mobile">
              <span class="d-block">{{ plan.call_reception }}</span>
              <span class="d-block">{{ plan.calls_per_week }}</span>
              <span class="d-block">{{ plan.agent }}</span>
            </div>
            <div>
              <button class="btn btn-primary w-100 plans-item-plan-btn">
                Subscribe Here
              </button>
            </div>
          </div>
        </div>

        <table class="plans-table w-100 mt-40">
          <tr>
            <td class="plans-logo p-10">Call Reception</td>
            <td class="plans-item p-10 text-center">
              {{ plans[0].call_reception }}
            </td>
            <td class="plans-item p-10 text-center">
              {{ plans[1].call_reception }}
            </td>
            <td class="plans-item p-10 text-center fw-700 text-primary">
              {{ plans[2].call_reception }}
            </td>
          </tr>
          <tr>
            <td class="plans-logo p-10">Call Reception</td>
            <td class="plans-item p-10 text-center">
              {{ plans[0].calls_per_week }}
            </td>
            <td class="plans-item p-10 text-center">
              {{ plans[1].calls_per_week }}
            </td>
            <td class="plans-item p-10 text-center fw-700 text-primary">
              {{ plans[2].calls_per_week }}
            </td>
          </tr>
          <tr>
            <td class="plans-logo p-10">Call Reception</td>
            <td class="plans-item p-10 text-center">{{ plans[0].agent }}</td>
            <td class="plans-item p-10 text-center">{{ plans[1].agent }}</td>
            <td class="plans-item p-10 text-center fw-700 text-primary">
              {{ plans[2].agent }}
            </td>
          </tr>
        </table>
      </div>
    </section>
    <!-- plans end -->

    <!-- Newsletter -->
    <section class="newsletter">
      <div class="max-container newsletter-inner pb-100">
        <div class="newsletter-container">
          <div>
            <h3 class="text-white text-center">
              Join thousands of entrepreneurs using PressOne to improve their
              business communications.
            </h3>
            <p class="text-white text-center">
              Ready to make your customers love your business?
            </p>
            <div class="mt-40 text-center">
              <button class="btn btn-secondary newsletter-btn">Join Now</button>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- Newsletter -->
  </main>
</template>

<script>
import axios from "axios";
export default {
  name: "MainBody",
  data() {
    return {
      plans: [],
      data: [
        {
          id: 1,
          name: "Starter Plan",
          amount: "25000",
          description: "For businesses with few customers",
          cta: "Subscribe Here",
          call_reception: "Receive calls only",
          calls_per_week: "Less than 30 calls per week",
          agent: "Shared agents",
        },
        {
          id: 2,
          name: "Growth Plan",
          amount: "50000",
          description: "For growing businesses",
          cta: "Subscribe Here",
          call_reception: "Receive and make calls",
          calls_per_week: "30 - 70 calls per week",
          agent: "Semi-dedicated agents",
        },
        {
          id: 3,
          name: "All Access",
          amount: "Custom",
          description: "For e-commerce and retail businesses",
          cta: "Calculate Your Cost",
          call_reception: "Receive and make calls",
          calls_per_week: "You choose",
          agent: "Fully dedicated agents",
        },
      ],
      fetchTry: 0,
    };
  },
  methods: {
    async fetchPlans() {
      try {
        this.fetchTry++;
        const response = await axios.get("https://api.jsonserve.com/swQ1ic");
        if (response.status == 200) {
          console.log("here too");
          this.plans = response.data.data;
        } else {
          if (this.fetchTry < 5) {
            setTimeout(() => {
              console.log(this.fetchTry);
              this.fetchPlans();
            }, 300000);
          }
        }
      } catch (err) {
        if (this.fetchTry < 5) {
          setTimeout(() => {
            console.log(this.fetchTry);
            this.fetchPlans();
          }, 300000);
        }
      }
    },
    formatPrice(value) {
      if (value.toLowerCase() == "custom") {
        return value;
      } else {
        return "N" + value.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",");
      }
    },
  },
  created() {
    this.plans = this.data;
    this.fetchPlans();
  },
};
</script>

<style lang="scss">
$basic-color: #0e99d2;

.more {
  position: relative;
  left: 0;
  right: 0;
  width: 100vw;
  &-info {
    gap: 2%;
    justify-content: space-between;
    padding: 120px 0 80px;
    margin-top: 70px;

    @media screen and (max-width: 1200px) {
      flex-wrap: wrap;
    }

    &-item {
      border-radius: 10px;
      background: #f3f8fe;
      flex-basis: 20%;
      padding: 70px 9px 20px 8px;
      max-width: 400px;
      border: 15px solid #fff;

      @media screen and (max-width: 1200px) {
        flex-basis: 40%;
        margin-bottom: 60px;
      }

      @media screen and (max-width: 600px) {
        flex-basis: 100%;
      }

      &-icon-wrapper {
        left: 0;
        top: -58px;
      }

      &-icon-cover {
        background: #f3f8fe;
        border: 12px solid #fff;
        text-align: center;
        width: 60px;
        height: 60px;
        padding: 10px;
        top: -90%;
        position: relative;
        border-radius: 90px;
      }

      &-icon {
        margin-top: 12px;
      }
    }
  }
}

.services {
  padding-top: 130px;
  margin-top: -75px;
  background: url(../assets/images/svg/mid-left-bkg.svg),
    url(../assets/images/svg/mid-right-bkg.svg);
  background-position: left top, right bottom;
  background-repeat: no-repeat, no-repeat;

  &-inner {
    @media screen and (max-width: 800px) {
      flex-wrap: wrap;
    }
  }

  &-item {
    flex-basis: 40%;
    max-width: 450px;
    display: flex;

    &-inner {
      display: flex;
      flex-direction: column;

      @media screen and (max-width: 800px) {
        flex-basis: 100%;
        margin-bottom: 30px;
      }
    }

    &-top {
      height: 190px;
      border-radius: 20px 24px 0px 0px;
      background-repeat: no-repeat;

      &-1 {
        background: url("../assets/images/img/services-1.png");
      }

      &-2 {
        background: url("../assets/images/img/services-2.png");
      }
    }

    &-bottom {
      background: #fff;
      border-radius: 20px;
      box-shadow: rgba(0, 0, 0, 0.01) 0px 1px 3px 0px,
        rgba(27, 31, 35, 0.08) 0px 0px 0px 1px;
      margin-top: -15px;
      flex: 1;

      &-icon {
        &-wrapper {
          left: 0;
          top: -77px;
        }
        &-cover {
          text-align: center;
          padding: 10px;
          position: relative;
        }
      }

      &-text {
        padding: 45px 20px;
      }
    }
  }
}

.plans {
  &-container {
    z-index: 100;
    position: relative;
  }

  @media screen and (max-width: 1000px) {
    flex-wrap: wrap;
  }

  &-logo {
    flex-basis: 19%;

    @media screen and (max-width: 1000px) {
      flex-basis: 45%;
      img {
        width: 100px;
      }
    }

    @media screen and (max-width: 600px) {
      flex-basis: 100%;
    }
  }

  &-item {
    flex-basis: 27%;

    &-plan {
      padding: 20px;
      flex-basis: 25%;
      box-shadow: rgba(0, 0, 0, 0.01) 0px 1px 3px 0px,
        rgba(27, 31, 35, 0.15) 0px 0px 0px 1px;
      border-radius: 12px;

      @media screen and (max-width: 1000px) {
        flex-basis: 40%;
      }

      @media screen and (max-width: 600px) {
        flex-basis: 100%;
      }

      &-info {
        &-mobile {
          border-top: 1px solid rgba(27, 31, 35, 0.15);
          padding: 20px 0;
          display: none;

          @media screen and (max-width: 1000px) {
            display: block;
          }
        }
      }

      &-btn {
        padding: 14px 0;
        font-size: 16px;
      }
    }
  }

  &-table {
    border-collapse: collapse;

    @media screen and (max-width: 1000px) {
      display: none;
    }

    tr {
      &:nth-child(odd) {
        background-color: #eaf1f6;
      }

      td {
        &:first-child {
          border-radius: 8px 0px 0px 8px;
        }
        &:last-child {
          border-radius: 0px 8px 8px 0px;
        }
      }
    }
  }
}

.newsletter {
  margin-top: -100px;

  &-inner {
    padding-top: 220px;
    background: url(../assets/images/svg/b4footer-left-bkg.svg);
    background-position: left top;
    background-repeat: no-repeat, no-repeat;
  }
  &-container {
    width: 60%;
    max-width: 1400px;
    margin: 0 auto;
    border-radius: 20px;
    padding: 30px 40px;
    background: url(../assets/images/svg/inbtw-left-bkg.svg),
      url(../assets/images/svg/inbtw-right-bkg.svg), $basic-color;
    background-position: left top, right bottom;
    background-repeat: no-repeat, no-repeat;

    @media screen and (max-width: 600px) {
      width: 85%;
    }

    @media screen and (max-width: 400px) {
      width: 95%;
      padding: 30px 10px;
    }

    h3 {
      word-break: break-all;
    }
  }

  &-btn {
    padding: 14px 90px;

    @media screen and (max-width: 400px) {
      width: 100%;
      padding: 14px 0;
    }
  }
}
</style>
