<template>
  <div class="base-input">
    <input value="" placeholder="Email" />
    <label>Email</label>
  </div>
</template>

<style scoped lang="scss">
.base-input {
  position: relative;
  display: inline-block;
  > input {
    border: 1px solid #afafaf;
    border-radius: 7px;
    background-color: transparent;
    outline: none;
    padding: 12px 16px;
    color: #1a1a1a;
    font-size: 16px;
    z-index: 1;
    transition: 0.25s;
    &:focus {
      border-color: #7D17E6;
      box-shadow: 0 0 0 0 rgb(0 0 0 / 15%);
      -webkit-box-shadow: 0 0 0 0 rgb(0 0 0 / 15%);
      + label {
        transform: translate(-2px, -22px);
        color: #7D17E6;
        font-size: 14px;
        font-weight: 400;
      }
    }
    &::placeholder {
      opacity: 0;
      transition: inherit;
    }
    &:not(:placeholder-shown) + label {
      font-size: 14px;
      transform: translate(-2px, -22px);
    }
  }
  > label {
    color: #afafaf;
    position: absolute;
    left: 10px;
    top: 10px;
    transition: 0.25s;
    background-color: #ffffff;
    font-size: 16px;
    font-weight: 300;
    padding: 0 3px;
    z-index: 0;
    pointer-events: none;
    cursor: pointer;
  }
}
</style>
