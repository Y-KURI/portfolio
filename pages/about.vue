<template>
  <div class="container">
    <img class="about-author__img" src="~/static/sign.jpg" alt="">
    <table class="about-table">
      <tr>
        <td class="term">Name:</td>
        <td class="desc">{{ name }}</td>
      </tr>
      <tr>
        <td class="term">Location:</td>
        <td class="desc">{{ location }}</td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  data: () => ({
    name:	'Kurihara',
    location:	'Kanagawa'
  })
}
</script>

<style>
.container {
  flex-direction: column;
}
.about-author__img{
  width: 280px;
  border-radius: 50%;
}
.about-table {
  width: 90%;
  border-radius: 5px;
  background-color: white;
  align-items: flex-start;
  padding: 2rem;
  font-size: 20px;
}
.term {
  text-align: right;
}
.desc {
  text-align: left;
  padding-left: 15px;
}
</style>
