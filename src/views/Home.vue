<template>
  <div class="page-wrapper">
    <section class="main-content-wrapper">
      <div class="app-wrapper">
        <div class="app-inner-bg">
          <div class="app-header">
            <svg class="menu-arrow" width="4" height="10" viewBox="0 0 4 10" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M2.10557 0.552784C2.35256 0.0588057 2.95324 -0.141419 3.44721 0.105571C3.90591 0.334918 4.11131 0.869227 3.94056 1.33989L3.89443 1.44721L2.118 5L3.89443 8.55278C4.12377 9.01148 3.96751 9.56217 3.54851 9.83625L3.44721 9.89443C2.98852 10.1238 2.43783 9.96751 2.16374 9.54851L2.10557 9.44721L0.105573 5.44721C-0.0150818 5.2059 -0.0323182 4.92797 0.0538637 4.6762L0.105573 4.55278L2.10557 0.552784Z" fill="white"/>
            </svg>

            <div class="header-user">
              <img src="@/assets/img/avatar.jpg" alt="Samuel Green" />

              <div class="user-content">
                <p class="username">Samuel Green</p>
                <p class="status">Available to Walk</p>
              </div>
            </div>

            <svg class="menu-dots" width="2" height="8" viewBox="0 0 2 8" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path fill-rule="evenodd" clip-rule="evenodd" d="M2 1C2 1.55228 1.55228 2 1 2C0.447715 2 0 1.55228 0 1C0 0.447715 0.447715 0 1 0C1.55228 0 2 0.447715 2 1ZM2 4C2 4.55228 1.55228 5 1 5C0.447715 5 0 4.55228 0 4C0 3.44772 0.447715 3 1 3C1.55228 3 2 3.44772 2 4ZM1 8C1.55228 8 2 7.55228 2 7C2 6.44772 1.55228 6 1 6C0.447715 6 0 6.44772 0 7C0 7.55228 0.447715 8 1 8Z" fill="white"/>
            </svg>
          </div>

          <div class="app-interface">
            <div class="user-messages">
              <div class="user-message message-block">
                <p>That sounds great. I’d be happy with that.</p>
              </div>
              <div class="user-message message-block">
                <p>Could you send over some pictures of your dog, please?</p>
              </div>
            </div>

            <div class="partner-messages">
              <div class="partner-message img-block">
                <img src="@/assets/img/dog-image-1.jpg" alt="Dog Picture 1" />
                <img src="@/assets/img/dog-image-2.jpg" alt="Dog Picture 2" />
                <img src="@/assets/img/dog-image-3.jpg" alt="Dog Picture 3" />
              </div>

              <div class="partner-message message-block">
                <p>Here are a few pictures. She’s a happy girl!</p>
              </div>
              <div class="partner-message message-block">
                <p>Can you make it?</p>
              </div>
            </div>

            <div class="user-messages">
              <div class="user-message message-block">
                <p>She looks so happy! The time we discussed works. How long shall I take her out for?</p>
              </div>

              <div class="user-message choice-block">
                <span class="radio-button"></span>
                <p class="choice-text">30 minute walk</p>
                <p class="choice-price">$29</p>
              </div>

              <div class="user-message choice-block">
                <span class="radio-button"></span>
                <p class="choice-text">30 minute walk</p>
                <p class="choice-price">$29</p>
              </div>
            </div>

            <div class="submit-wrapper">
              <p>Type a message...</p>
              <span class="submit-icon">
                <svg width="7" height="10" viewBox="0 0 7 10" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M1.06419 0.464993C1.50167 0.028436 2.19006 -0.00514531 2.66614 0.364249L2.78047 0.464993L6.42125 4.09809C6.85873 4.53464 6.89238 5.22158 6.52221 5.69666L6.42125 5.81074L2.78047 9.44384C2.30653 9.91677 1.53813 9.91677 1.06419 9.44384C0.626713 9.00728 0.59306 8.32034 0.963236 7.84527L1.06419 7.73118L3.84588 4.95442L1.06419 2.17765C0.626713 1.74109 0.59306 1.05416 0.963236 0.579081L1.06419 0.464993Z" fill="white"/>
                </svg>
              </span>
            </div>
          </div>
        </div>
      </div>

      <div class="content-wrapper">
        <h1>Simple booking</h1>

        <p>
          Stay in touch with our dog walkers through the chat interface.
          This makes it easy to discuss arrangements and make bookings. Once the walk has been completed you can
          rate your walker and book again all through the chat.</p>
      </div>
    </section>
  </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
  head() {
    return {
      title: {
        inner: 'Home'
      },
      meta: [
        {
          name: 'description',
          content: `${this.appTitle} home page`,
          id: 'desc'
        }
      ]
    }
  },
  computed: mapState('app', ['appTitle'])
}
</script>

<style lang="scss" scoped>
@import '@/theme/variables.scss';
@import '@/theme/main-content.scss';

.page-wrapper {
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  height: 100%;
  width: 100%;
  overflow: hidden;

  &:before,
  &:after {
    content: '';
    position: absolute;
    display: block;
    width: 510px;
    height: calc(85vh + 255px);
    z-index: 1;
    border-radius: 255px;
  }

  &:before {
    top: -255px;
    left: -90px;
    background: $gradientColor;

    @media (max-width: 1000px) {
      left: -180px;
    }

    @media (max-width: 900px) {
      top: -55vh;
    }

    @media (max-width: 600px) {
      left: -270px;
    }

    @media (max-width: 400px) {
      left: -320px;
    }
  }

  &:after {
    bottom: -255px;
    right: -185px;
    background: $gradientColor;
    opacity: 0.03;

    @media (max-width: 900px) {
      bottom: -55vh;
    }

    @media (max-width: 600px) {
      right: -285px;
    }

    @media (max-width: 400px) {
      right: -325px;
    }
  }
}
</style>
