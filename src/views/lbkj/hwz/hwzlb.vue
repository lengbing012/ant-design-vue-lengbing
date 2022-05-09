<template>
  <div>
    {{msg}}
  </div>
</template>

<script>
  import {getAction} from '@/api/manage'

  export default {
    name: 'hwzlb',
    data(){
      return{
        msg: ""
      }
    },
    methods: {
      wz(){
        let url = "/lbkj/hwz"
        getAction(url).then((res) => {
          //console.log("返回数据",res)
          if(res.success){
            this.msg = res.result;
          }
        })
      }
    },
    created(){
      this.wz();
    }
  }
</script>

<style scoped>

</style>