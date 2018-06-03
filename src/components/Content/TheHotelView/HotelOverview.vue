<template>
  <div class="overview">
    <h1 class="overview__heading">
      Hotel Las Palmas
    </h1>
    <div class="overview__stars">
      <svg class="overview__icon-star" version="1.1" xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 20 20">
        <title>star</title>
        <path d="M10 1.3l2.388 6.722h6.412l-5.232 3.948 1.871 6.928-5.439-4.154-5.438 4.154 1.87-6.928-5.233-3.948h6.412l2.389-6.722z"></path>
      </svg>
      <svg class="overview__icon-star" version="1.1" xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 20 20">
        <title>star</title>
        <path d="M10 1.3l2.388 6.722h6.412l-5.232 3.948 1.871 6.928-5.439-4.154-5.438 4.154 1.87-6.928-5.233-3.948h6.412l2.389-6.722z"></path>
      </svg>
      <svg class="overview__icon-star" version="1.1" xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 20 20">
        <title>star</title>
        <path d="M10 1.3l2.388 6.722h6.412l-5.232 3.948 1.871 6.928-5.439-4.154-5.438 4.154 1.87-6.928-5.233-3.948h6.412l2.389-6.722z"></path>
      </svg>
      <svg class="overview__icon-star" version="1.1" xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 20 20">
        <title>star</title>
        <path d="M10 1.3l2.388 6.722h6.412l-5.232 3.948 1.871 6.928-5.439-4.154-5.438 4.154 1.87-6.928-5.233-3.948h6.412l2.389-6.722z"></path>
      </svg>
      <svg class="overview__icon-star" version="1.1" xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 20 20">
        <title>star</title>
        <path d="M10 1.3l2.388 6.722h6.412l-5.232 3.948 1.871 6.928-5.439-4.154-5.438 4.154 1.87-6.928-5.233-3.948h6.412l2.389-6.722z"></path>
      </svg>
    </div>
    <div class="overview__location">
      <svg class="overview__icon-location" version="1.1" xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 20 20">
        <title>location-pin</title>
        <path d="M10 2.009c-2.762 0-5 2.229-5 4.99 0 4.774 5 11 5 11s5-6.227 5-11c0-2.76-2.238-4.99-5-4.99zM10 9.76c-1.492 0-2.7-1.209-2.7-2.7s1.208-2.7 2.7-2.7c1.49 0 2.699 1.209 2.699 2.7s-1.209 2.7-2.699 2.7z"></path>
      </svg>
      <button class="btn-inline">Lagos, Nigeria</button>
    </div>
    <div class="overview__rating">
      <div class="overview__rating-average">8.6</div>
      <div class="overview__rating-count">429 votes</div>
    </div>
  </div>
</template>


<style lang="scss" scoped>
  .overview {
    display: flex;
    align-items: center;
    border-bottom: 1px solid var(--color-grey-light-4);
    &__heading {
      font-size: 2.25rem;
      font-weight: 300;
      text-transform: uppercase;
      letter-spacing: 1px;
      padding: 1.5rem 3rem;


     @media only screen and (max-width: 37.5em) {
       font-size: 1.8rem;
       padding: 1.25rem 2rem;
      }
    }
    &__stars {
      margin-right: auto; // neat trick to occupy space
      display: flex;
    }
    &__icon-star,
    &__icon-location {
      width: 1.75rem;
      height: 1.75rem;
      fill: var(--color-primary-2);
    }
    &__location {
      font-size: 1.2rem;
      display: flex;
      align-items: center;
    }
    &__icon-location {
      margin-right: .5rem;
    }
    &__rating {
      background-color: var(--color-primary-2);
      color: #fff;
      margin-left: 3rem;
      padding: 0 2.25rem;
      align-self: stretch; //stretches items top to bottom
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;

      @media only screen and (max-width: 37.5em) {
       padding: 0 1.5rem;
      }
    }
    &__rating-average {
      font-size: 2.25rem;
      font-weight: 300;
      margin-bottom: -3px;

      @media only screen and (max-width: 37.5em) {
       font-size: 1.8rem;
      }
    }
    &__rating-count {
      font-size: .8rem;
      text-transform: uppercase;

       @media only screen and (max-width: 37.5em) {
       font-size: .5rem;
      }
    }
  } ////////////////////////////////////////
  // BUTTON INLINE
  .btn-inline {
    border: none;
    color: var(--color-primary-2);
    font-size: inherit;
    border-bottom: 1px solid currentColor;
    padding-bottom: 2px;
    display: inline-block;
    background-color: transparent;
    cursor: pointer;
    transition: all .2s;

    & span {
      margin-left: 3px; // show all button 
      transition: margin-left .2s;

    }

    &:hover {
      color: var(--color-grey-dark-1);
      span {
        margin-left: 8px; // show all button 
      }
    }
    &:focus {
      outline: none;
      animation: pulsate 1s infinite;
    }
    @keyframes pulsate {
      0% {
        transform: scale(1);
        box-shadow: none;
      }
      50% {
        transform: scale(1.05);
        box-shadow: 0 1rem 4rem rgba(0, 0, 0, .25);
      }
      100% {
        transform: scale(1);
        box-shadow: none;
      }
    }
  }
</style>