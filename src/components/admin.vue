<template>
  <div>
    <span @click="routerClick">Admin...</span>
  </div>
</template>

<script>
export default {
  mounted(){
    console.log(this.$route.params.name);
    console.log(this.$store.state.tableData);
  },
  methods:{
    routerClick(){
      this.$store.dispatch('addUser',{name:'Mr丶Cps',address:'上海市杨浦区复旦绿地双创中心',date:'2018-08-08'});
      this.$router.push({ name: 'home', params: { name: 'home' }})
    }
  }
}
</script>

<style>

</style>
