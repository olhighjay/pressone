<template>
  <section class="hero-banner w-100 max-container">
    <div class="hero-section">
      <div class="d-flex header-container hero-text-cover">
        <!-- left texts -->
        <div class="mr-auto hero-text">
          <h1>
            You do the work, <br />
            We’ll do the talk
          </h1>
          <h3 class="mt--10">
            Move your customers’ <span class="text-primary">enquiry</span> to
            our team of experts
          </h3>
          <p>
            Let us manage your customer relationship from their first call till
            they become your raving fans
          </p>
          <div class="mt-60">
            <button class="btn btn-primary get-started-btn">Get Started</button>
          </div>
        </div>

        <!-- right image -->
        <div class="hero-img">
          <img class="w-100" src="../assets/images/img/11176.png" alt="" />
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
.hero-banner {
  background-image: url(../assets/images/svg/top-right-bkg.svg),
    url(../assets/images/svg/top-left-bkg.svg);
  background-position: right, left top;
  background-repeat: no-repeat, no-repeat;
  position: relative;
  padding-bottom: 40px;

  .hero-section {
    margin-top: 49px;
    padding-top: 120px;

    @media screen and (max-width: 1000px) {
      margin-top: 0;
    }
  }

  .hero-text-cover {
    gap: 10%;

    @media screen and (max-width: 1000px) {
      flex-wrap: wrap;
    }
  }

  .hero-text {
    flex-basis: 60%;

    @media screen and (max-width: 1000px) {
      flex-basis: 100%;
    }

    p {
      color: #616c74;
      font-family: Urbanist;
      font-size: 20px;
      font-style: normal;
      font-weight: 500;
      margin-top: -18px;
      line-height: 140%;
    }

    .get-started-btn {
      border: none;
      font-size: 18px;
      padding: 14px 110px;
      border-radius: 4px;

      @media screen and (max-width: 380px) {
        width: 100%;
        padding: 14px 0;
      }
    }
  }

  .hero-img {
    @media screen and (max-width: 1000px) {
      flex-basis: 100%;
      margin-top: 80px;
    }
  }
}
</style>
