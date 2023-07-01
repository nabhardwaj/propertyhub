<template >
  <div class="slider-box">
  <div class="item">
    <i>
      <slot name="icon"></slot>
    </i>
    <div class="details">
      <h3>
        <slot name="heading"></slot>
      </h3>
      <slot></slot>
    </div>
  </div>
  </div>
</template>

<style scoped>

.slider-box{
  background: #e6ffcb;
  display: block;
  position: relative;
  min-height:60vh;
}
.item {
  background: url('../assets/images/banner-bg.webp') ;
  background-size: contain;
  display: flex;
  position: relative;
  text-align: center;
  min-height: inherit;
  place-items: center;
}
.item:before{
  content: '';
  display: block;
  position:absolute;
  top: 0px;
  left: 0px;
  background: rgba(230,255,203,0.5);
  width:100%;
  min-height:60vh;
}
.details {
  flex: 1;
  position: relative;
  color: #616161;
  font-size: 1rem;
}

i {
  display: flex;
  place-items: center;
  place-content: center;
  width: 32px;
  height: 32px;
  color: var(--color-text);
}

h3 {
  font-size: 1.2rem;
  font-weight: 500;
  margin-bottom: 0.4rem;
  color: var(--color-text);
}

@media (min-width: 1024px) {
  /* .item {
    margin-top: 0;
  } */

  i {
    top: calc(50% - 25px);
    left: -26px;
    position: absolute;
    border: 1px solid var(--color-border);
    background: var(--color-background);
    border-radius: 8px;
    width: 50px;
    height: 50px;
  }

  /* .item:before {
    content: ' ';
    border-left: 1px solid var(--color-border);
    position: absolute;
    left: 0;
    bottom: calc(50% + 25px);
    height: calc(50% - 25px);
  }

  .item:after {
    content: ' ';
    border-left: 1px solid var(--color-border);
    position: absolute;
    left: 0;
    top: calc(50% + 25px);
    height: calc(50% - 25px);
  } */

  /* .item:first-of-type:before {
    display: none;
  }

  .item:last-of-type:after {
    display: none;
  } */
}
</style>
