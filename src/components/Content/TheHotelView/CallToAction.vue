<template>
  <div class="cta">
    <h2 class="cta__book-now">
      Good news! We have 4 free rooms for your selected dates!
    </h2>
    <button class="btn">
      <span class="btn__visible">Book now</span>
      <span class="btn__invisible">Only 4 rooms left</span>
    </button>
  </div>
</template>

<style lang="scss" scoped>
  .cta {
    padding: 3.5rem 0;
    text-align: center;

     @media only screen and (max-width: 56.75em) {
     padding: 2rem 0;

    }

    &__book-now {
      font-size: 2rem;
      font-weight: 300;
      text-transform: uppercase;
      margin-bottom: 2.5rem;
    }
  }

  .btn{
    font-size: 1.5rem;
    font-weight: 400;
    text-transform: uppercase;
    border-radius: 5px;
    border: none;
    background-image: linear-gradient(to right, var(--color-primary-light), var(--color-primary-dark));
    color: white;
    position: relative;
    overflow: hidden;

    & > *{
      display: inline-block;
      height: 100%;
      width: 100%; 
      transition: all .2s;

    }

    &__visible{
      padding: 2rem 7.5rem;
    }
    &__invisible{
      position: absolute;
      padding: 2rem 0;
      left: 0;
      top: -100%; 
    }
    &:hover{
      background-image: linear-gradient(to left, var(--color-primary-light), var(--color-primary-dark));

    }
    &:hover &__visible{
      transform: translateY(100%)
    }
    &:hover &__invisible{
      top:0;
    }
    &:focus{
      outline: none;
      animation: pulsate 1s infinite;
    }
  }
</style>