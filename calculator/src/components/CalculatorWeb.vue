<template>
  <div class="calculator">
     <DisplayCalculator msg="displayValue" />
      <ButtonCalculator label="AC" triple @onClick="clearMemory" />
      <ButtonCalculator label="/" operation @onClick="setOperation" />
      <ButtonCalculator label="7" @onClick="addDigit" />
      <ButtonCalculator label="8" @onClick="addDigit" />
      <ButtonCalculator label="9" @onClick="addDigit" />
      <ButtonCalculator label="*" operation @onClick="setOperation" />
      <ButtonCalculator label="4" @onClick="addDigit" />
      <ButtonCalculator label="5" @onClick="addDigit" />
      <ButtonCalculator label="6" @onClick="addDigit" />
      <ButtonCalculator label="-" operation @onClick="setOperation" />
      <ButtonCalculator label="1" @onClick="addDigit" />
      <ButtonCalculator label="2" @onClick="addDigit" />
      <ButtonCalculator label="3" @onClick="addDigit" />
      <ButtonCalculator label="+" operation @onClick="setOperation" />
      <ButtonCalculator label="0" double @onClick="addDigit" />
      <ButtonCalculator label="." @onClick="addDigit" />
      <ButtonCalculator label="=" operation @onClick="setOperation" />

   
  </div>
</template>

<script>
import DisplayCalculator from './Display.vue'
import ButtonCalculator from './Button.vue'
export default {
  name: 'CalculatorWeb',
  components: {
      DisplayCalculator,ButtonCalculator,

  }


}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
.calculator {
    height: 320px;
    width: 235px;
    border-radius: 5px;
    overflow: hidden;
    display: grid;
    grid-template-columns: repeat(4, 25%);
    grid-template-rows: 1fr 48px 48px 48px 48px 48px;
}
</style>