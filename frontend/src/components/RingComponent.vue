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
      <option value="optionX">Option X</option>
      <option value="optionY">Option Y</option>
      <option value="optionZ">Option Z</option>
    </select>

    <!-- Range -->
    <label for="range1">Range 1:</label>
    <input type="range" id="range1" v-model="range1" @input="handleRange1Input" />
    <span>{{ range1 }}</span>

    <!-- Range -->
    <label for="range2">Range 2:</label>
    <input type="range" id="range2" v-model="range2" @input="handleRange2Input" />
    <span>{{ range2 }}</span>

    <!-- Selection -->
    <label for="selection3">Selection 3:</label>
    <select id="selection3" v-model="selection3">
      <option value="optionM">Option M</option>
      <option value="optionN">Option N</option>
      <option value="optionO">Option O</option>
    </select>

    <!-- Selection -->
    <label for="selection4">Selection 4:</label>
    <select id="selection4" v-model="selection4">
      <option value="optionP">Option P</option>
      <option value="optionQ">Option Q</option>
      <option value="optionR">Option R</option>
    </select>

    <!-- Selection -->
    <label for="selection5">Selection 5:</label>
    <select id="selection5" v-model="selection5">
      <option value="optionS">Option S</option>
      <option value="optionT">Option T</option>
      <option value="optionU">Option U</option>
    </select>

    <!-- Range -->
    <label for="range3">Range 3:</label>
    <input type="range" id="range3" v-model="range3" @input="handleRange3Input" />
    <span>{{ range3 }}</span>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selection1: "",
      selection2: "",
      range1: 0,
      range2: 0,
      selection3: "",
      selection4: "",
      selection5: "",
      range3: 0,
    };
  },
  methods: {
    handleRange1Input() {
      // Handle Range 1 input if needed
    },
    handleRange2Input() {
      // Handle Range 2 input if needed
    },
    handleRange3Input() {
      // Handle Range 3 input if needed
    },
  },
};
</script>

<style scoped>
</style>