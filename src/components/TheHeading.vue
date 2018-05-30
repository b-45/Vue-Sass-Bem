<template>
  <header class="header">
    <img src="../img/logo.png" alt="" class="logo">
    <form action="#" class="search">
      <input type="text" class="search__input" placeholder="Search hotels">
      <button class="search__button">
        <svg class="search__icon" version="1.1" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 20 20">
          <title>magnifying-glass</title>
          <path d="M17.545 15.467l-3.779-3.779c0.57-0.935 0.898-2.035 0.898-3.21 0-3.417-2.961-6.377-6.378-6.377s-6.186 2.769-6.186 6.186c0 3.416 2.961 6.377 6.377 6.377 1.137 0 2.2-0.309 3.115-0.844l3.799 3.801c0.372 0.371 0.975 0.371 1.346 0l0.943-0.943c0.371-0.371 0.236-0.84-0.135-1.211zM4.004 8.287c0-2.366 1.917-4.283 4.282-4.283s4.474 2.107 4.474 4.474c0 2.365-1.918 4.283-4.283 4.283s-4.473-2.109-4.473-4.474z"></path>
        </svg>
      </button>
    </form>
    <nav class="user-nav">
      <div class="user-nav__icon-box">
        <svg class="user-nav__icon">
          <svg version="1.1" xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 20 20">
            <title>bookmark</title>
            <path d="M14 2v17l-4-4-4 4v-17c0-0.553 0.585-1.020 1-1h6c0.689-0.020 1 0.447 1 1z"></path>
          </svg>
        </svg>
        <span class="user-nav__notification">7</span>
      </div>
      <div class="user-nav__icon-box">
        <svg class="user-nav__icon">
          <svg version="1.1" xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 20 20">
            <title>chat</title>
            <path d="M5.8 12.2v-6.2h-3.8c-1.1 0-2 0.9-2 2v6c0 1.1 0.9 2 2 2h1v3l3-3h5c1.1 0 2-0.9 2-2v-1.82c-0.064 0.014-0.132 0.021-0.2 0.021l-7-0.001zM18 1h-9c-1.1 0-2 0.9-2 2v8h7l3 3v-3h1c1.1 0 2-0.899 2-2v-6c0-1.1-0.9-2-2-2z"></path>
          </svg>
        </svg>
        <span class="user-nav__notification">11</span>
      </div>
      <div class="user-nav__user">
        <img src="../img/user.jpg" alt="User photo" class="user-nav__user-photo">
        <span class="user-nav__user-name">Bernard Ade</span>
      </div>
    </nav>
  </header>
</template>

<style lang="scss" scoped>
  .header {
    font-size: 1.4rem;
    height: 7rem;
    background-color: #fff;
    border-bottom: 1px solid var(--color-grey-light-2);
    display: flex;
    justify-content: space-between;
    align-items: center;

     @media only screen and (max-width: 31.25em) {
       flex-wrap: wrap;
       align-content: space-around;
       height: 11rem;
    }
  }

  .logo {
    height: 3.25rem;
    margin-left: 2rem; // margin from the left
  }

  .search {
    flex: 0 0 40%;
    display: flex;
    align-items: center;
    justify-content: center;

    @media only screen and (max-width: 31.25em) {
      order: 1;
      flex: 0 0 100%;
      background-color: var(--color-grey-light-2);

    }

    &__input {
      font-family: inherit;
      font-size: inherit;
      background-color: var(--color-grey-light-2);
      border: none;
      padding: .7rem 2rem; // padding .7 top/bottom and 2rem left/right
      border-radius: 3px;
      width: 90%;
      transition: all .2s;
      margin-right: -3.25rem; //move button on top of input
      &:focus {
        outline: none;
        width: 100%;
        background-color: var(--color-grey-light-3);
      }
      &::-webkit-input-placeholder {
        font-weight: 100;
        color: var(--color-grey-light-4);
      }
    }
    &__input:focus+&__button {
      background-color: var(--color-grey-light-3);
    }
    &__button {
      border: none;
      background-color: var(--color-grey-light-2);
      &:focus {
        outline: none;
      }
      &:active {
        transform: translateY(2px);
      }
    }
    &__icon {
      height: 2rem;
      width: 2rem;
      fill: var(--color-grey-dark-3);
    }
  }

  .user-nav {
    display: flex;
    align-items: center;
    align-self: stretch; //overides align center in header to stretch so user nav can fill height of parent header
    &>* {
      padding: 0 2rem;
      cursor: pointer;
      height: 100%;
      display: flex;
      align-items: center;
    }
    &>*:hover {
      background-color: var(--color-grey-light-2);
    }
    &__icon-box {
      position: relative;
    }
    &__icon {
      height: 2.25rem;
      width: 2.25rem;
      fill: var(--color-grey-dark-2);
    }
    &__notification {
      font-size: .8rem;
      height: 1.75rem;
      width: 1.75rem;
      border-radius: 50%;
      background-color: var(--color-primary-2);
      color: #fff;
      position: absolute;
      top: 1.5rem;
      right: 1.1rem;
      display: flex;
      justify-content: center;
      align-items: center;
    }
    &__user-photo {
      height: 3.75rem;
      border-radius: 50%;
      margin-right: 1rem;
    }
  }
</style>