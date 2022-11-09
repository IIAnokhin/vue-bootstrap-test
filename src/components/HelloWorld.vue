<template>
  <div class="container">
    <b-card bg-variant="dark" text-variant="white" title="Checkbox">
      <b-card-text>
        {{ status }}
      </b-card-text>
    </b-card>
    <div class="combobox">
      <b-form-group label="Combobox" v-slot="{ ariaDescribedby }">
        <b-form-radio-group
          v-model="selected"
          :options="options"
          :aria-describedby="ariaDescribedby"
          name="radio-inline"
        ></b-form-radio-group>
      </b-form-group>
      <div class="mt-3">
        Option: <strong>{{ selected }}</strong>
      </div>
    </div>
    <div>
    <b-form-textarea
      id="textarea"
      placeholder="Enter something..."
      rows="3"
      max-rows="6"
    ></b-form-textarea>

    
    
  </div>
  </div>
</template>
<script>
export default {
  props: ["status"],
  data() {
    return {
      selected: "first",
      options: [
        { text: "First option", value: "first" },
        { text: "Second option", value: "second" },
        { text: "Third option", value: "third" },
      ],
    };
  },
};
</script>
<style scoped>
.container {
  display: flex;
  flex-direction: column;
  height: 100%;
  margin-top: 30px;
}
.combobox {
  margin-top: 30px;
  margin-bottom: 30px;
  padding: 16px;
  border: 1px solid grey;
  border-radius: 6px;
}
</style>
