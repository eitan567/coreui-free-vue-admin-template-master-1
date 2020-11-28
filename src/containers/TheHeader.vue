<template>
  <CHeader fixed with-subheader light>
    <CToggler
      in-header
      class="ml-3 d-lg-none"
      @click="$store.commit('toggleSidebarMobile')"
    />
    <CToggler
      in-header
      class="ml-3 d-md-down-none"
      @click="$store.commit('toggleSidebarDesktop')"
    />
    <CHeaderBrand class="mx-auto d-lg-none" to="/">
      <CIcon name="logo" height="48" alt="Logo" />
    </CHeaderBrand>
    <CHeaderNav class="d-md-down-none mr-auto">
      <CHeaderNavItem class="px-3">
        <CHeaderNavLink to="/dashboard"> Dashboard </CHeaderNavLink>
      </CHeaderNavItem>
      <CHeaderNavItem class="px-3">
        <CHeaderNavLink to="/users" exact> Users </CHeaderNavLink>
      </CHeaderNavItem>
      <CHeaderNavItem class="px-3">
        <CHeaderNavLink> Settings </CHeaderNavLink>
      </CHeaderNavItem>
    </CHeaderNav>
    <CHeaderNav class="mr-4">
      <CHeaderNavItem class="d-md-down-none mx-2">
        <CHeaderNavLink>
          <CIcon name="cil-bell" />
        </CHeaderNavLink>
      </CHeaderNavItem>
      <CHeaderNavItem class="d-md-down-none mx-2">
        <CHeaderNavLink>
          <CIcon name="cil-list" />
        </CHeaderNavLink>
      </CHeaderNavItem>
      <CHeaderNavItem class="d-md-down-none mx-2">
        <CHeaderNavLink>
          <CIcon name="cil-envelope-open" />
        </CHeaderNavLink>
      </CHeaderNavItem>
      <TheHeaderDropdownAccnt />
    </CHeaderNav>
    <CSubheader class="px-2 pt-2">
      <!-- <CBreadcrumbRouter class="border-0 mb-0"/> -->      
          <CRow class="col-lg-12 pb-3">
            <CCol sm="4">
              <b-form-group
                label-cols-sm="3"
                label="מתאריך : "
                label-size="sm"
                label-class="font-weight-bold pt-0"
                class="mb-0 pt-1"
              >
                <b-form-datepicker
                  id="example-datepicker"
                  v-model="value"
                  class="col-sm-9 col-md-9"
                ></b-form-datepicker
              ></b-form-group>
            </CCol>
            <CCol sm="4">
              <b-form-group
                label-cols-sm="3"
                label="מתאריך : "
                label-size="sm"
                label-class="font-weight-bold pt-0"
                class="mb-0 pt-1"
              >
                <b-form-datepicker
                  id="example-datepicker1"
                  v-model="value"
                  class="col-sm-9 col-md-9"
                ></b-form-datepicker
              ></b-form-group>
            </CCol>
            <CCol sm="4">
              <b-form-group
                label-cols-sm="3"
                label="מתאריך : "
                label-size="sm"
                label-class="font-weight-bold pt-0"
                class="mb-0 pt-1"
              >
                <b-form-datepicker
                  id="example-datepicker2"
                  v-model="value"
                  class="col-sm-9 col-md-9"
                ></b-form-datepicker
              ></b-form-group>
            </CCol>
          </CRow>
        
    </CSubheader>
  </CHeader>
</template>

<script>
import TheHeaderDropdownAccnt from "./TheHeaderDropdownAccnt";

export default {
  name: "TheHeader",
  components: {
    TheHeaderDropdownAccnt,
  },
  data() {
    return {
      value: "",
    };
  },
};
</script>
