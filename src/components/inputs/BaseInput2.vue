<template>
  <div class="base-input">
    <span>https://</span>
    <input value="" placeholder="domain.xyz" />
  </div>
</template>

<style scoped lang="scss">
.base-input {
  position: relative;
  display: flex;
  width: 100%;
  > input {
    display: block;
    width: 100%;
    padding: 8px 16px;
    line-height: 25px;
    font-size: 14px;
    font-weight: 500;
    -webkit-appearance: none;
    color: #99A3BA;
    border-radius: 0 6px 6px 0;
    border: 1px solid #afafaf;
    background: #ffffff;
    transition: border 0.3s ease;
    &::placeholder {
      color: #CBD1DC;
    }
    &:focus {
      outline: none;
      border-color: #7D17E6;
    }
  }
  > span {
    border-radius: 6px 0 0 6px;
    text-align: center;
    padding: 8px 12px;
    font-size: 14px;
    line-height: 25px;
    color: #99A3BA;
    background: #EEF4FF;
    border: 1px solid #afafaf;
    transition: all 0.3s ease;
  }
  &:focus-within {
    & > span {
      color: #ffffff;
      background-color: #7D17E6;
      border-color: #7D17E6;
    }
  }
}
</style>
