<template>
    <div>
      <!-- Selection -->
      <label for="selection1">Selection 1:</label>
      <select id="selection1" v-model="selection1">
        <option value="option1">Option 1</option>
        <option value="option2">Option 2</option>
        <option value="option3">Option 3</option>
      </select>
  
      <!-- Selection -->
      <label for="selection2">Selection 2:</label>
      <select id="selection2" v-model="selection2">
        <option value="optionA">Option A</option>
        <option value="optionB">Option B</option>
        <option value="optionC">Option C</option>
      </select>
  
      <!-- Number to number range -->
      <label for="range1">Number Range 1:</label>
      <input type="number" id="range1-min" v-model="range1.min" @input="validateRange1" />
      <span class="range-separator">to</span>
      <input type="number" id="range1-max" v-model="range1.max" @input="validateRange1" />
      <span v-if="range1.error" class="error-message">{{ range1.error }}</span>
  
      <!-- Number to number range -->
      <label for="range2">Number Range 2:</label>
      <input type="number" id="range2-min" v-model="range2.min" @input="validateRange2" />
      <span class="range-separator">to</span>
      <input type="number" id="range2-max" v-model="range2.max" @input="validateRange2" />
      <span v-if="range2.error" class="error-message">{{ range2.error }}</span>
  
      <!-- Number to number range -->
      <label for="range3">Number Range 3:</label>
      <input type="number" id="range3-min" v-model="range3.min" @input="validateRange3" />
      <span class="range-separator">to</span>
      <input type="number" id="range3-max" v-model="range3.max" @input="validateRange3" />
      <span v-if="range3.error" class="error-message">{{ range3.error }}</span>
  
      <!-- Selection -->
      <label for="selection3">Selection 3:</label>
      <select id="selection3" v-model="selection3">
        <option value="optionX">Option X</option>
        <option value="optionY">Option Y</option>
        <option value="optionZ">Option Z</option>
      </select>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        selection1: "",
        selection2: "",
        range1: { min: null, max: null, error: null },
        range2: { min: null, max: null, error: null },
        range3: { min: null, max: null, error: null },
        selection3: "",
      };
    },
    methods: {
      validateRange1() {
        this.range1.error = this.validateRange(this.range1.min, this.range1.max);
      },
      validateRange2() {
        this.range2.error = this.validateRange(this.range2.min, this.range2.max);
      },
      validateRange3() {
        this.range3.error = this.validateRange(this.range3.min, this.range3.max);
      },
    },
  };
  </script>
  
  <style scoped>
  </style>