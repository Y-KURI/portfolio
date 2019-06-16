<template>
  <nav class="header">
    <ul class="gnav__items">
      <li class="gnav__item" ><nuxt-link  class="gnav__link" to="/">Top</nuxt-link></li>
      <li class="gnav__item" ><nuxt-link  class="gnav__link" to="about">About</nuxt-link></li>
      <li class="gnav__item" ><nuxt-link  class="gnav__link" to="works">Works</nuxt-link></li>
      <li class="gnav__item" ><nuxt-link  class="gnav__link" to="skills">Skills</nuxt-link></li>
      <li class="gnav__item" ><nuxt-link  class="gnav__link" to="contact">Contact</nuxt-link></li>
    </ul>
  </nav>
</template>

<style>
.header {
  background-color: #41b883;
}

.gnav__items {
  display: flex;
  width: 100%;
  padding: 0;
}
.gnav__item {
  flex: 1;
  list-style: none;
}

.gnav__link {
  display: flex;
  height: 70px;
  align-items: center;
  justify-content: center;
  color: #fff;
  font-size: 20px;
  font-weight: 500;
  font-family: 'M PLUS Rounded 1c', sans-serif;
}

.gnav__link:hover {
  background-color: gold;
}

.nuxt-link-exact-active {
  background: #F5F5F5;
  color: #41b883;
}

</style>
