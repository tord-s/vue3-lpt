<template>
  <div class="container">
    <router-link to="/">
      <a href="https://example.com" target="_blank" rel="noopener noreferrer">
        <img src="@/assets/logo.png" alt="logo" id="logo" />
      </a>
    </router-link>
    <router-link to="/about" class="nav_link">About</router-link>
    <router-link to="/lorem" class="nav_link">Lorem</router-link>
    <router-link to="/ipsum" class="nav_link">Ipsum</router-link>
    <router-link to="/contact" class="nav_link">Contact</router-link>
    <Toggle :lightMode="lightMode" @toggle="$emit('toggle')" />
  </div>
</template>

<script>
import Toggle from "@/components/Toggle";
export default {
  props: ["lightMode"],
  components: {
    Toggle,
  },
};
</script>

<style scoped>
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: var(--header-padding);
  height: var(--header-height);
}
#logo {
  width: 100px;
  height: auto;
}
.nav_link {
  padding: 0.5vw 2vw 0.5vw 2vw;
  margin: 2vw;
  font-size: 1.5em;
  text-decoration: none;
  border-bottom: transparent solid 2px;
}
.nav_link:hover,
.nav_link.router-link-active {
  border-bottom: #a8bbb0 solid 2px;
  transition: 0.5s;
}
</style>
