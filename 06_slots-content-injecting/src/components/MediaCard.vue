<template>
  <div class="media-card">
    <div class="media-card-image">
      <slot name="image">
        <img src="https://images.unsplash.com/photo-1495835788122-ca48931258be?ixlib=rb-0.3.5&ixid=eyJhcHBfaWQiOjEyMDd9&s=acc48b0187b28f7a221362b843f15755&auto=format&fit=crop&w=3450&q=80" alt="">
      </slot>
    </div>
    <div class="media-card-content">
      <h4 class="media-card-heading">
        <slot name="heading">
          Default card heading goes here
        </slot>
      </h4>
      <div class="media-card-body">
        <slot>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Officia eos accusantium minima architecto natus sequi quisquam incidunt dolorem, adipisci accusamus facere dicta magni, qui consectetur, omnis quis, voluptas tempore quo!</p>
        </slot>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'MediaCard'
  }
</script>

<style>
  .media-card {
    background-color: #fff;
    border-radius: 0.5rem;
    overflow: hidden;
    box-shadow: 0 15px 30px 0 rgba(0, 0, 0, 0.11),
    0 5px 15px 0 rgba(0, 0, 0, 0.08);
  }
  .media-card-image {
    height: 10rem;
    overflow: hidden;
  }
  .media-card-image > img {
    height: 100%;
    width: 100%;
    object-fit: cover;
    object-position: center;
  }
  .media-card-content {
    padding: 1.5rem;
  }
  .media-card-heading {
    margin-bottom: 1rem;
    font-size: 1rem;
    line-height: 1.25;
    color: #22292f;
  }
  .media-card-body {
    font-size: 0.875rem;
    color: #3d4852;
    line-height: 1.5;
  }
</style>
