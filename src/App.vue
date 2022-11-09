<template>
  <div id="app">
    <div>
      <b-navbar type="dark" variant="dark">
        <b-navbar-nav>
          <b-nav-item href="#">Home</b-nav-item>
          <b-nav-item>
            <b-button variant="success">Success</b-button>
          </b-nav-item>
          <div class="checkbox-item">
            
            <b-form-checkbox
              id="checkbox-1"
              v-model="status"
              name="checkbox-1"
              value="accepted"
              unchecked-value="not_accepted"
              >
              </b-form-checkbox>
          </div>
          
          <!-- Navbar dropdowns -->
          <b-nav-item-dropdown text="Lang" right>
            <b-dropdown-item href="#">EN</b-dropdown-item>
            <b-dropdown-item href="#">ES</b-dropdown-item>
            <b-dropdown-item href="#">RU</b-dropdown-item>
            <b-dropdown-item href="#">FA</b-dropdown-item>
          </b-nav-item-dropdown>

          <b-nav-item-dropdown text="User" right>
            <b-dropdown-item href="#">Account</b-dropdown-item>
            <b-dropdown-item href="#">Settings</b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-navbar>
    </div>
    <HelloWorld :status="status"/>
    <GridTest/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import GridTest from './components/GridTest.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    GridTest
  },
  data() {
      return {
        status: 'not_accepted',
      }
    }
}
</script>
<style scoped>
.checkbox-item {
  margin: auto;
  margin-left: 20px;
  margin-right: 20px;
}
</style>

