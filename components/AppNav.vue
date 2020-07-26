<template>
  <header>
    <h1>Candy Shop 🍬</h1>
    <nav>
      <ul>
        <li>
          <nuxt-link exact to="/">Home</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/all">All</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/prints">Prints</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/men">Men</nuxt-link>
        </li>
        <li>
          <div class="carttotal" v-if="cartCount > 0">{{ cartCount }}</div>
          <nuxt-link to="/cart">Cart</nuxt-link>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
import { mapGetters } from "vuex";

export default {
  computed: {
    ...mapGetters(["cartCount"])
  }
};
</script>

<style lang="scss" scoped>
header {
  display: inline-flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  background-color: aquamarine;
  padding-left: 10px;
  position: fixed;
  top: 0;
  z-index: 3;
  h1 {
    font-family: 'Bangers', cursive;
    color: darkslategrey;
    margin: 0;
    flex: 1;
    font-size: 20px;
  }
}

nav {
  display: flex;
  flex: 3;
  justify-content: center;
  align-items: center;
  padding: 8px 0;
  ul {
    padding-left: 0;
    li {
      display: inline;
      text-transform: uppercase;
      letter-spacing: 0.1em;
      font-size: 13px;
      padding: 0 20px;
      position: relative;
      a {
        color: black;
        &:hover {
          color: #c14103;
        }
      }
    }
  }
}

.carttotal {
  position: absolute;
  border-radius: 1000px;
  background: black;
  color: white;
  font-size: 10px;
  padding: 3px;
  top: -18px;
  right: -5px;
  width: 25px;
  text-align: center;
  height: 25px;
  font-size: 10px;
  padding: 6px 10px;
  font-weight: bold;
}

@media screen and (max-width: 850px) {
  h1 {
    margin: 0;
  }
  nav ul li {
    padding: 0 5px !important;
    border-left: none !important;
    border-right: none !important;
  }
}
</style>