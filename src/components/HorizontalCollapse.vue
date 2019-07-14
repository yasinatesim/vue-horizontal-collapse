<template>
  <section class="js-horizontal-collapse  horizontal-collapse">
    <ul class="horizontal-collapse__inner">
      <HorizontalCollapseItem className="horizontal-collapse__item--1">
        <div class="horizontal-collapse__inactive-content">
          <h2 class="horizontal-collapse__heading">One inactive</h2>
        </div>
        <div class="horizontal-collapse__active-content">
          <h2 class="horizontal-collapse__heading">One active</h2>
          <p class="horizontal-collapse__body">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptates
            modi laudantium facere aut, nemo praesentium, labore doloremque,
            porro ipsam qui nihil animi ea maiores. Ut excepturi quae veritatis.
            Recusandae, cupiditate? Lorem ipsum dolor sit amet consectetur
            adipisicing elit. Voluptates modi laudantium facere aut, nemo
            praesentium, labore doloremque, porro ipsam qui nihil animi ea
            maiores. Ut excepturi quae veritatis. Recusandae, cupiditate?
          </p>
        </div>
      </HorizontalCollapseItem>

      <HorizontalCollapseItem className="horizontal-collapse__item--2">
        <div class="horizontal-collapse__inactive-content">
          <h2 class="horizontal-collapse__heading">Two inactive</h2>
        </div>
        <div class="horizontal-collapse__active-content">
          <h2 class="horizontal-collapse__heading">Two active</h2>
          <p class="horizontal-collapse__body">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptates
            modi laudantium facere aut, nemo praesentium, labore doloremque,
            porro ipsam qui nihil animi ea maiores. Ut excepturi quae veritatis.
            Recusandae, cupiditate? Lorem ipsum dolor sit amet consectetur
            adipisicing elit. Voluptates modi laudantium facere aut, nemo
            praesentium, labore doloremque, porro ipsam qui nihil animi ea
            maiores. Ut excepturi quae veritatis. Recusandae, cupiditate?
          </p>
        </div>
      </HorizontalCollapseItem>

      <HorizontalCollapseItem className="horizontal-collapse__item--3">
        <div class="horizontal-collapse__inactive-content">
          <h2 class="horizontal-collapse__heading">Three inactive</h2>
        </div>
        <div class="horizontal-collapse__active-content">
          <h2 class="horizontal-collapse__heading">Three active</h2>
          <p class="horizontal-collapse__body">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptates
            modi laudantium facere aut, nemo praesentium, labore doloremque,
            porro ipsam qui nihil animi ea maiores. Ut excepturi quae veritatis.
            Recusandae, cupiditate? Lorem ipsum dolor sit amet consectetur
            adipisicing elit. Voluptates modi laudantium facere aut, nemo
            praesentium, labore doloremque, porro ipsam qui nihil animi ea
            maiores. Ut excepturi quae veritatis. Recusandae, cupiditate?
          </p>
        </div>
      </HorizontalCollapseItem>

      <HorizontalCollapseItem className="horizontal-collapse__item--4">
        <div class="horizontal-collapse__inactive-content">
          <h2 class="horizontal-collapse__heading">Four inactive</h2>
        </div>
        <div class="horizontal-collapse__active-content">
          <h2 class="horizontal-collapse__heading">Four active</h2>
          <p class="horizontal-collapse__body">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptates
            modi laudantium facere aut, nemo praesentium, labore doloremque,
            porro ipsam qui nihil animi ea maiores. Ut excepturi quae veritatis.
            Recusandae, cupiditate? Lorem ipsum dolor sit amet consectetur
            adipisicing elit. Voluptates modi laudantium facere aut, nemo
            praesentium, labore doloremque, porro ipsam qui nihil animi ea
            maiores. Ut excepturi quae veritatis. Recusandae, cupiditate?
          </p>
        </div>
      </HorizontalCollapseItem>

      <HorizontalCollapseItem className="horizontal-collapse__item--5">
        <div class="horizontal-collapse__inactive-content">
          <h2 class="horizontal-collapse__heading">Five inactive</h2>
        </div>
        <div class="horizontal-collapse__active-content">
          <h2 class="horizontal-collapse__heading">Five active</h2>
          <p class="horizontal-collapse__body">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptates
            modi laudantium facere aut, nemo praesentium, labore doloremque,
            porro ipsam qui nihil animi ea maiores. Ut excepturi quae veritatis.
            Recusandae, cupiditate? Lorem ipsum dolor sit amet consectetur
            adipisicing elit. Voluptates modi laudantium facere aut, nemo
            praesentium, labore doloremque, porro ipsam qui nihil animi ea
            maiores. Ut excepturi quae veritatis. Recusandae, cupiditate?
          </p>
        </div>
      </HorizontalCollapseItem>
    </ul>
  </section>
</template>

<script>
import HorizontalCollapseItem from "./HorizontalCollapseItem";

export default {
  name: "HorizontalCollapse",
  components: {
    HorizontalCollapseItem
  }
};
</script>

<style lang="scss">
$transitionDurationMs: 0.5s;

.horizontal-collapse {
  width: 100%;
  margin: 0 auto;
  display: flex;
  flex-direction: row;
  justify-content: center;
  margin-bottom: 5rem;
  color: #fff;

  *,
  *:before,
  *:after {
    box-sizing: border-box;
  }

  &__inner {
    padding: 0;
    margin: 0;
    display: flex;
    flex-direction: row;
  }

  &__item {
    min-height: 42rem;
    list-style: none;
    padding: 0;
    overflow: hidden;
    min-width: 10rem;
    max-width: 40rem;
    position: relative;
    transition: width $transitionDurationMs;

    &--1 {
      background-color: red;
    }

    &--2 {
      background-color: green;
    }

    &--3 {
      background-color: blue;
    }

    &--4 {
      background-color: purple;
    }

    &--5 {
      background-color: orange;
    }

    &.is-active {
      // color: #fff;

      .horizontal-collapse__inactive-content {
        opacity: 0;
      }

      .horizontal-collapse__active-content {
        opacity: 1;
      }
    }
  }

  &__item-inner {
    padding: 3rem;
  }

  &__inactive-content {
    opacity: 1;
    transition: opacity $transitionDurationMs;
    position: absolute;
    bottom: 2rem;
    left: 1rem;

    .horizontal-collapse__heading {
      user-select: none;
      cursor: default;
      font-size: 3rem;
      line-height: 0;
      margin-bottom: 0;
      writing-mode: vertical-rl;
      text-orientation: mixed;
      transform: rotate(180deg);
    }
  }

  &__active-content {
    opacity: 0;
    transition: opacity $transitionDurationMs;
    cursor: default;
  }

  &__heading {
    margin-top: 0;
    margin-bottom: 2rem;
  }

  &__body {
    margin-bottom: 2rem;
  }

  &__link {
    display: inline-block;
    background-color: #fff;
    color: #333;
    text-decoration: none;
    line-height: 1;
    padding: 1rem 2rem;
    border-radius: 2rem;
    font-size: 1.7rem;
    font-weight: bold;
  }
}
</style>
