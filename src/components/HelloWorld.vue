<template>
  <div class="hello">
    <NavMenu></NavMenu>
    <div>{{msg}}</div>
    <div class="danger">{{warn}}</div>
    <Home></Home>
    <Button @reseveMsg="reseve"></Button>
    <PickDate></PickDate>
    <FormName v-if="show_header == 'bool'"></FormName>
  </div>
</template>

<script>
import Home from '@/views/Home'
import Button from '@/views/Button'
import NavMenu from '@/views/NavMenu'
import PickDate from '@/views/PickDate'
import FormName from '@/views/FormName'

export default {
  name: 'HelloWorld',
  props: {
    msg: String,
  },
  data () {
    return {
      msg2:'',
      show_header:'bool'
    }
  },
  components:{
    NavMenu,
    Home,
    Button,
    PickDate,
    FormName
  },
  methods:{
    reseve(payload){
      this.msg2 = payload
    }
  },
  computed:{
    warn:function (){
      let warnMsg=(this.msg2?(this.msg2+'!'):"")
      return warnMsg
    }
  }
}
</script>
<style scoped>
  .danger{color:red}
</style>
