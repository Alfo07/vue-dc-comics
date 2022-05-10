<template>
  <header>
    <div class="logo">
      <img src="../assets/dc-logo.png" alt="" />
      <nav>
        <ul>
          <li
            v-for="(item, index) in links"
            :key="index"
            :class="{ selected: item.active }"
          >
            {{ item.testo }}
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "AppHeader",
  data() {
    return {
      links: [
        {
          testo: "Characters",
          link: "",
          active: true,
        },
        {
          testo: "Comics",
          link: "",
          active: false,
        },
        {
          testo: "Movies",
          link: "",
          active: false,
        },
        {
          testo: "TV",
          link: "",
          active: false,
        },
        {
          testo: "Games",
          link: "",
          active: false,
        },
        {
          testo: "Collectibles",
          link: "",
          active: false,
        },
        {
          testo: "Videos",
          link: "",
          active: false,
        },
        {
          testo: "Fans",
          link: "",
          active: false,
        },
        {
          testo: "News",
          link: "",
          active: false,
        },
        {
          testo: "Shop",
          link: "",
          active: false,
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import '../style/vars';
@import '../style/generals';
.logo {
  display: flex;
  justify-content: space-around;
  img {
    width: 5%;
    padding: 10px;
  }
}
nav {
  background-color: $bgwhite;
  display: flex;
  align-items: center;
}
li {
  text-transform: uppercase;
  list-style-type: none;
  display: inline-block;
  justify-content: space-around;
  padding: 34px 12px;
  font-size: 13px;
  cursor: pointer;
}
.selected {
  border-bottom: 5px solid $bgazzurro;
  color: $bgazzurro;
}
</style>
