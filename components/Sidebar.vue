<template>
  <div>
    <b-button class="btn-sidebar" v-b-toggle.sidebar-backdrop
      ><b-icon icon="arrow-right"></b-icon
    ></b-button>

    <div>
      <b-sidebar
        id="sidebar-backdrop"
        title="Sidebar with backdrop"
        :backdrop-variant="variant"
        backdrop
        shadow
      >
        <div class="px-3 py-2"></div>
      </b-sidebar>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      variant: "dark"
    };
  }
};
</script>

<style>
.btn-sidebar {
  position: fixed;
  left: 5px;
  top: 50%;
}
</style>
