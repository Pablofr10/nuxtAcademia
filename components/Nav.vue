<template>
  <div>
    <b-navbar toggleable="lg" type="dark" variant="dark">
      <b-navbar-brand href="#">Nuxt Fitt</b-navbar-brand>
      <b-button v-b-toggle.sidebar-backdrop
        ><b-icon icon="camera"></b-icon
      ></b-button>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item href="#">Link</b-nav-item>
          <b-nav-item href="#" class="active">Disabled</b-nav-item>
        </b-navbar-nav>
        <b-navbar-nav class="ml-auto">
          <b-nav-item-dropdown text="Lang" right>
            <b-dropdown-item href="#">EN</b-dropdown-item>
            <b-dropdown-item href="#">ES</b-dropdown-item>
            <b-dropdown-item href="#">RU</b-dropdown-item>
            <b-dropdown-item href="#">FA</b-dropdown-item>
          </b-nav-item-dropdown>

          <b-nav-item-dropdown right>
            <!-- Using 'button-content' slot -->
            <template #button-content>
              <em>Perfil</em>
            </template>
            <b-dropdown-item href="#">Profile</b-dropdown-item>
            <b-dropdown-item href="#">Sign Out</b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>

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

<style scoped></style>
