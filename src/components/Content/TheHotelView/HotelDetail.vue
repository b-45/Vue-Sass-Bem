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