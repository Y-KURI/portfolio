<template>
  <div class="container">
    <table class="contact_table">
      <tr>
        <td class="term">Twitter:</td>
        <td class="desc"><a href="https://twitter.com/__castagna">{{ twitter }}</a></td>
      </tr>
      <tr>
        <td class="term">Gmail:</td>
        <td class="desc">{{ gmail }}</td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  data: () => ({
    twitter:	'@__castagna',
    gmail:	'yasuaki6@gmail.com'
  })
}
</script>

<style>
.contact_table {
  width: 90%;
  border-radius: 5px;
  background-color: white;
  padding: 2rem;
  font-size: 20px;
}
</style>
