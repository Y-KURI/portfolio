<template>
  <div class="container">
    <table class="skill_table">
      <tr>
        <td class="skill_term">Langs:</td>
        <td class="skill_desc" v-for="lang in langs" :key="lang">{{ lang.name }}</td>
      </tr>
      <tr>
        <td class="skill_term">Frameworks:</td>
        <td class="skill_desc" v-for="framework in frameworks" :key="framework">{{ framework.name }}</td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  data: () => ({
    langs:	[
      { name: 'HTML' },
      { name: 'css' },
      { name: 'javascript' },
      { name: 'Ruby' },
      { name: 'Python' } ],
    frameworks:	[
      { name: 'Rails' },
      { name: 'Bootstrap' },
      { name: 'Vuejs' }]
  })

}
</script>

<style>
.skill_table {
  width: 90%;
  border-radius: 5px;
  background-color: white;
  padding: 2rem;
  font-size: 20px;
}
.skill_term {
  text-align: right;
  padding-top: 0px;
  padding-right: 20px;
}
.skill_desc {
  text-align: left;
  padding-left: 10px;
  padding-right: 1px;
}
</style>
