<template>
  <nav class="gnav header">
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
.gnav {
  display: flex;
}

.gnav__items {
  display: flex;
  flex: 1;
  list-style: none;
}

.gnav__item {
  flex: 1;
  text-decoration: none;
}
.gnav__link {
  align-items: center;
  text-decoration: none;
  color: #fff;
  font-weight: 500;
}

.header {
  font-size: 20px;
  left: 0;
  top: 0;
  width: 100%;
  background-color: #59bb0c;
  color: #fff;
}

</style>
