<template>
  <div class="form-container">
    <label for="itemSelection">{{ labels.selection }}</label>
    <select id="itemSelection" v-model="formData.selection" @change="handleSelectionChange">
      <option v-for="option in selectionOptions" :key="option" :value="option">{{ option }}</option>
    </select>

    <div class="component-container">
      <RingComponent v-if="isRingComponentVisible" />

      <CommonComponent v-else-if="isCommonComponentVisible" v-model="formData.range" :label="labels.range" />
    </div>
  </div>
</template>

<script>
import RingComponent from './RingComponent.vue';
import CommonComponent from './CommonComponent.vue';

export default {
  components: {
    RingComponent,
    CommonComponent
  },
  data() {
    return {
      currentField: ['selection'],
      formData: {
        selection: '',
        text: '',
        range: '',
      },
      labels: {
        selection: 'Select Item',
        range: 'Range',
      },
      selectionOptions: ['Armbånd', 'Armringe', 'Halskæder', 'Ringe', 'Vedhæng', 'Øreringe', 'Manchetknapper'],
    };
  },
  computed: {
    isRingComponentVisible() {
      return this.currentField.includes('range') && this.formData.selection.includes('Ringe');
    },
    isCommonComponentVisible() {
      return this.currentField.includes('range') && !this.isRingComponentVisible;
    },
  },
  methods: {

    handleSelectionChange() {
      this.currentField = ['range'];
    },
    handleSelectionInput(selectedItem) {
      this.formData.selection = selectedItem;
      this.nextField();
    },
    nextField() {
      this.currentField.push('range');
    },
  }
};
</script>

<style scoped>
.form-container {
  max-width: 400px;
  /* Set the maximum width of your form */
  margin: auto;
  /* Center the form horizontally */
  padding: 20px;
  /* Add some padding for better readability */
}

.component-container {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  /* Align components to the start of the column */
  margin-top: 20px;
  /* Add some spacing between the selection dropdown and components */
}

/* Additional styling for each component */
.component-container>* {
  margin-bottom: 10px;
  /* Add margin between each component */
}
</style>