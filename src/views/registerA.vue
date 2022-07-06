<template>
  <div id="main">
    <div id="a">
      <a href="javascript:" @click="mobileFn">手机注册</a>
      <a href="javascript:" @click="mailboxFn">邮箱注册</a>
    </div>
    <div>
      <keep-alive>
        <component :is="comName"></component>
      </keep-alive>
    </div>
    <LoginPassword v-slot="scoped">
      <input type="text" v-model="scoped.row.password" placeholder="登录密码" />
      <input type="text" v-model="scoped.row.passwordAgin" />
      <input type="text" v-model="scoped.row.invitation" placeholder="邀请码" />
    </LoginPassword>
  </div>
</template>

<script>
import MobileRegistration from '../components/registerAAA/MobileRegistration.vue'
import MailboxRegistration from '../components/registerAAA/MailboxRegistration.vue'
import LoginPassword from '../components/registerAAA/LoginPassword.vue'

export default {
  data() {
    return {
      comName: 'MobileRegistration',
    }
  },
  methods: {
    mobileFn() {
      this.comName = MobileRegistration
    },
    mailboxFn() {
      this.comName = MailboxRegistration
    },
  },
  components: {
    MobileRegistration,
    MailboxRegistration,
    LoginPassword,
  },
}
</script>

<style scoped>
#main {
  background-color: skyblue;
  width: 300px;
  height: 600px;
  padding: 20px 20px;
}
input {
  height: 30px;
  margin-bottom: 15px;
}
#a {
  margin-bottom: 15px;
  font-size: 22px;
}
</style>
