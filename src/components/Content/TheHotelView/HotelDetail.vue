<template>
  <div class="detail">
    <div class="description">
      <p class="paragraph">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolor voluptas veniam veritatis culpa impedit rerum optio accusamus
        nobis, harum nihil labore distinctio nostrum eveniet ducimus hic.
      </p>
      <p class="paragraph">
        Dolor voluptas veniam veritatis culpa impedit rerum optio accusamus nobis, harum nihil labore distinctio nostrum eveniet
        ducimus hic.
      </p>

      <ul class="list">
        <li class="list__item">Close to the Beach</li>
        <li class="list__item">Breakfast included</li>
        <li class="list__item">Free airport shuttle</li>
        <li class="list__item">Free wifi in all rooms</li>
        <li class="list__item">Air conditioning and heating</li>
        <li class="list__item">Pets allowed</li>
        <li class="list__item">We speak all language</li>
        <li class="list__item">Perfect for families</li>
      </ul>
      <div class="recommend">
        <p class="recommend__count">
          Lucy and 3 other friends recommend this hotel.
        </p>
        <div class="recommend__friends">
          <img src="../../../img/user-2.jpg" alt="Friends 1" class="recommend__photo">
          <img src="../../../img/user-4.jpg" alt="Friends 2" class="recommend__photo">
          <img src="../../../img/user-5.jpg" alt="Friends 3" class="recommend__photo">
          <img src="../../../img/user-6.jpg" alt="Friends 4" class="recommend__photo">
        </div>
      </div>
    </div>

    <div class="user-reviews">
      <figure class="user-reviews">
        <figure class="review">
          <blockquote class="review__text">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Amet quae obcaecati porro vitae saepe sit atque optio?
          </blockquote>
          <figcaption class="review__user">
            <img src="../../../img/user-6.jpg" alt="User 1" class="review__photo">
            <div class="review__user-box">
              <p class="review__user-name">Anna Smith</p>
              <p class="review__user-date">Feb 23rd, 2017</p>
            </div>
            <div class="review__rating">7.8</div>
          </figcaption>
        </figure>

        <figure class="review">
          <blockquote class="review__text">
            Dolor sit amet consectetur adipisicing elit. Amet quae obcaecati porro vitae saepe sit atque optio?
          </blockquote>
          <figcaption class="review__user">
            <img src="../../../img/user-1.jpg" alt="User 1" class="review__photo">
            <div class="review__user-box">
              <p class="review__user-name">Nick Thomas</p>
              <p class="review__user-date">Sep 23rd, 2017</p>
            </div>
            <div class="review__rating">7.8</div>
          </figcaption>
        </figure>
        <button class="btn-inline">Show all
          <span>&rarr;</span>
        </button>
      </figure>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .detail {
    font-size: 1.4rem;
    display: flex;
    padding: 4.5rem;
    background-color: var(--color-grey-light-1);
    border-bottom: var(--line);

     @media only screen and (max-width: 56.25em) { //900px/16px
     padding: 3rem;
    }

     @media only screen and (max-width: 37.5em) {  //600px/16px
     flex-direction: column;
    }
  }


  .description {
    background-color: #fff;
    box-shadow: var(--shadow-light);
    padding: 3rem;
    flex: 0 0 60%;
    margin-right: 4.5rem;

     @media only screen and (max-width: 56.75em) {
     padding: 2rem;
     margin-right: 3rem;
    }

    @media only screen and (max-width: 37.5em) {
     margin-right: 0rem;
     margin-bottom: 3rem;
    }
  }

  .user-reviews {
    flex: 1;
    display: flex;
    flex-direction: column;
    align-items: center;
  }


  .paragraph:not(:last-of-type) {
    margin-bottom: 2rem;
  }

  .list {
    list-style: none;
    margin: 3rem 0;
    padding: 3rem 0;
    border-top: var(--line);
    border-bottom: var(--line);
    display: flex;
    flex-wrap: wrap;
    &__item {
      flex: 0 0 50%;
      margin-bottom: .7rem;
    }
    &__item::before {
      content: "";
      display: inline-block;
      height: 1rem;
      width: 1rem;
      margin-right: .7rem;

      @supports (-webkit-mask-image: url() or (mask-image:url())) {
        background-color: var(--color-primary);
        -webkit-mask-image: url(../../../img/chevron-thin-right.svg);
        -webkit-mask-size: cover;
        mask-image: url(../../../img/chevron-thin-right.svg); //without prefixes for when other browsers implement this method
        mask-size: cover;
        background-image: none;
      }
    }
  }

  .recommend {
    font-size: 1.3rem;
    color: var(--color-grey-dark-3);
    display: flex;
    align-items: center;
    &__count {
      margin-right: auto; //pushes the box all the way to right 
    }
    &__friends {
      display: flex;
    }
    &__photo {
      box-sizing: content-box;
      height: 4rem;
      width: 4rem;
      border-radius: 50%;
      border: 3px solid #fff;
      &:not(:last-child) {
        margin-right: -2rem;
      }
    }
  }

  .review {
    background-color: #fff;
    box-shadow: var(--shadow-light);
    padding: 3em;
    margin-bottom: 3.5rem;
    position: relative; // reference to absolute positioning of quotation mark in top corner.
    overflow: hidden; //overflow for positioning of quotation mark in top corner.

     @media only screen and (max-width: 56.75em) {
     padding: 2rem;
     margin-bottom: 3rem;
    }
    &__text {
      margin-bottom: 2rem;
      z-index: 10;
      position: relative; //positioning for z-index
    }
    &__user {
      display: flex;
      align-items: center;
    }
    &__photo {
      height: 4.5rem;
      width: 4.5rem;
      border-radius: 50%;
    }
    &__user-box {
      margin-right: auto; //pushes the box all the way to right 
    }
    &__user-name {
      font-size: 1.1rem;
      font-weight: 600;
      text-transform: uppercase;
      margin-bottom: .4rem;
    }
    &__user-date {
      font-size: 1rem;
      color: var(--color-grey-dark-3);
    }
    &__rating {
      color: var(--color-primary);
      font-size: 2.2rem;
      font-weight: 300;
    }

    &::before {
      content: "\201C";
      position: absolute;
      top: -2.75rem;
      left: -1rem;
      line-height: 1;
      font-size: 20rem;
      color: var(--color-grey-light-2);
      font-family: sans-serif;
      z-index: 1;
    }
  }

  .btn-inline {
  border: none;
  color: var(--color-primary);
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