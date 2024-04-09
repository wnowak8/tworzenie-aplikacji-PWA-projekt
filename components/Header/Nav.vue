<script setup>
const navigation = [
  {
    label: "Sklep",
    link: "https://clickfashion.pl/sklep",
    children: [
      {
        label: "Kolekcja",
        link: "#",
      },
      {
        label: "Sukienki | Kombinezony",
        link: "#",
      },
      {
        label: "Bluzki | Koszule",
        link: "#",
      },
      {
        label: "Marynarki",
        link: "#",
      },
      {
        label: "Płaszcze | Kurtki",
        link: "#",
      },
      {
        label: "Spodnie",
        link: "#",
      },
      {
        label: "Spódnice",
        link: "#",
      },
      {
        label: "Swetry",
        link: "#",
      },
      {
        label: "Golfy",
        link: "#",
      },
    ],
  },
  {
    label: "Kolekcja zimowa",
    link: "https://clickfashion.pl/jesienzima.html",
  },
  {
    label: "Stylizacje wieczorowe",
    link: "https://clickfashion.pl/stylizacje-wieczorowe.html",
  },
  {
    label: "Stylizacje codzienne",
    link: "https://clickfashion.pl/stylizacje-codzienne.html",
  },
  {
    label: "Kolekcja świąteczna",
    link: "https://clickfashion.pl/kolekcja-swiateczna.html",
  },
  {
    label: "Wyprzedaż",
    link: "https://clickfashion.pl/sale-205.html",
  },
  {
    label: "Nowości",
    link: "https://clickfashion.pl/nowosci.html",
  },
];
</script>

<template>
  <nav>
    <ul>
      <li v-for="(item, index) of navigation" class="nav-item">
        <span class="nav-item-content">
          <a :href="item.link">{{ item.label }} </a>
          <span v-if="index === 0" class="material-symbols-outlined">
            expand_more
          </span>
        </span>
      </li>
      <div class="nav-item-children">
        <ul>
          <li v-for="item of navigation[0].children">
            <a :href="item.link">{{ item.label }} </a>
          </li>
        </ul>
      </div>
    </ul>
  </nav>
</template>

<style scoped lang="scss">
nav {
  padding: 10px 40px;
  width: 100%;
  max-width: 1600px;

  @media screen and (max-width: 1700px) {
    max-width: 1140px;
  }
}
ul {
  list-style: none;
  display: flex;
}
.nav-item {
  position: relative;
}

a {
  color: black;
  text-decoration: none;
  text-transform: uppercase;
}

.nav-item-content {
  display: flex;
  width: 100%;
  align-items: center;
  padding: 12px 20px;

  a {
    display: inline-block;
    position: relative;

    &::after {
      content: "";
      background: #000;
      height: 2px;
      width: 0;
      transition: 0.4s width ease-in-out;
      position: absolute;
      bottom: -13px;
      left: 0;
    }
  }

  &:hover {
    a::after {
      width: 100%;
    }
  }
}

.nav-item:first-child:hover ~ .nav-item-children,
.nav-item-children:hover {
  display: block;
}

.nav-item-children {
  position: absolute;
  display: none;
  left: 0;
  right: 0;
  top: 200px;
  background-color: #fff;

  ul {
    flex-direction: column;
    margin: 0 auto;
    padding: 10px 40px;
    width: 100%;
    max-width: 1600px;

    @media screen and (max-width: 1700px) {
      max-width: 1140px;
    }

    li {
      width: max-content;
      padding: 6px 8px;
      font-family: sans-serif;
      font-size: 14px;
      font-weight: bold;
      text-transform: uppercase;
    }
  }
}
</style>
