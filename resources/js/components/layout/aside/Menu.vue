<template>
  <ul class="menu-nav">
      <li
          aria-haspopup="true"
          data-menu-toggle="hover"
          class="menu-item menu-item-submenu"
          v-bind:class="{ 'menu-item-open': hasActiveChildren('/vue-bootstrap') }"
      >
          <a href="#" class="menu-link menu-toggle">
              <i class="menu-icon flaticon2-architecture-and-city"></i>
              <span class="menu-text">Master</span>
              <i class="menu-arrow"></i>
          </a>
          <div class="menu-submenu">
              <span class="menu-arrow"></span>
              <ul class="menu-subnav">
                  <li aria-haspopup="true" class="menu-item menu-item-parent">
            <span class="menu-link">
              <span class="menu-text">Master</span>
            </span>
                  </li>

                  <router-link
                      to="/users"
                      v-slot="{ href, navigate, isActive, isExactActive }"
                  >
                      <li v-index="$getConst('USER')"
                          aria-haspopup="true"
                          data-menu-toggle="hover"
                          class="menu-item"
                          :class="[
                isActive && 'menu-item-active',
                isExactActive && 'menu-item-active'
              ]"
                      >
                          <a :href="href" class="menu-link" @click="navigate">
                              <i class="menu-bullet menu-bullet-dot">
                                  <span></span>
                              </i>
                              <span class="menu-text">User Management</span>
                          </a>
                      </li>
                  </router-link>

                  <router-link
                      to="/role"
                      v-slot="{ href, navigate, isActive, isExactActive }"
                  >
                      <li v-index="$getConst('ROLE')"
                          aria-haspopup="true"
                          data-menu-toggle="hover"
                          class="menu-item"
                          :class="[
                isActive && 'menu-item-active',
                isExactActive && 'menu-item-active'
              ]"
                      >
                          <a :href="href" class="menu-link" @click="navigate">
                              <i class="menu-bullet menu-bullet-dot">
                                  <span></span>
                              </i>
                              <span class="menu-text">Role</span>
                          </a>
                      </li>
                  </router-link>

                  <router-link
                      to="/country"
                      v-slot="{ href, navigate, isActive, isExactActive }"
                  >
                      <li v-index="$getConst('COUNTRY')"
                          aria-haspopup="true"
                          data-menu-toggle="hover"
                          class="menu-item"
                          :class="[
                isActive && 'menu-item-active',
                isExactActive && 'menu-item-active'
              ]"
                      >
                          <a :href="href" class="menu-link" @click="navigate">
                              <i class="menu-bullet menu-bullet-dot">
                                  <span></span>
                              </i>
                              <span class="menu-text">Country</span>
                          </a>
                      </li>
                  </router-link>
                  <router-link
                      to="/state"
                      v-slot="{ href, navigate, isActive, isExactActive }"
                  >
                      <li v-index = "$getConst('STATE')"
                          aria-haspopup="true"
                          data-menu-toggle="hover"
                          class="menu-item"
                          :class="[
                isActive && 'menu-item-active',
                isExactActive && 'menu-item-active'
              ]"
                      >
                          <a :href="href" class="menu-link" @click="navigate">
                              <i class="menu-bullet menu-bullet-dot">
                                  <span></span>
                              </i>
                              <span class="menu-text">State</span>
                          </a>
                      </li>
                  </router-link>

                  <router-link
                      to="/city"
                      v-slot="{ href, navigate, isActive, isExactActive }"
                  >
                      <li v-index = "$getConst('CITY')"
                          aria-haspopup="true"
                          data-menu-toggle="hover"
                          class="menu-item"
                          :class="[
                isActive && 'menu-item-active',
                isExactActive && 'menu-item-active'
              ]"
                      >
                          <a :href="href" class="menu-link" @click="navigate">
                              <i class="menu-bullet menu-bullet-dot">
                                  <span></span>
                              </i>
                              <span class="menu-text">City</span>
                          </a>
                      </li>
                  </router-link>

                  <router-link
                      to="/hobby"
                      v-slot="{ href, navigate, isActive, isExactActive }"
                  >
                      <li v-index = "$getConst('HOBBY')"
                          aria-haspopup="true"
                          data-menu-toggle="hover"
                          class="menu-item"
                          :class="[
                isActive && 'menu-item-active',
                isExactActive && 'menu-item-active'
              ]"
                      >
                          <a :href="href" class="menu-link" @click="navigate">
                              <i class="menu-bullet menu-bullet-dot">
                                  <span></span>
                              </i>
                              <span class="menu-text">Hobby</span>
                          </a>
                      </li>
                  </router-link>
                  <router-link
                      to="/permission"
                      v-slot="{ href, navigate, isActive, isExactActive }"
                  >
                      <li v-index = "$getConst('PERMISSION')"
                          aria-haspopup="true"
                          data-menu-toggle="hover"
                          class="menu-item"
                          :class="[
                isActive && 'menu-item-active',
                isExactActive && 'menu-item-active'
              ]"
                      >
                          <a :href="href" class="menu-link" @click="navigate">
                              <i class="menu-bullet menu-bullet-dot">
                                  <span></span>
                              </i>
                              <span class="menu-text">Permission</span>
                          </a>
                      </li>
                  </router-link>
              </ul>
          </div>
      </li>
  </ul>
</template>

<script>
export default {
  name: "KTMenu",
  methods: {
    hasActiveChildren(match) {
      return this.$route["path"].indexOf(match) !== -1;
    }
  }
};
</script>
