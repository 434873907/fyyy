<template>
    <div>
        <!--<top>-->
            <!--<div class="middle big">注册</div>-->
        <!--</top>-->
        <top class="noflex" title="注册" ref="header">
            <i slot="back"></i>
        </top>
      <div>
        <div class="weui-cells__title">请输入手机号</div>
        <div class="weui-cells">
          <div class="weui-cell">
            <div class="weui-cell__bd">
              <input @blur="$v.mobile.$touch()" class="weui-input" type="number" v-model="mobile" placeholder="请输入"/>
            </div>
          </div>
        </div>
        <span class="form-group__message" v-show="!$v.mobile.phone&&showError">请输入正确的手机号</span>
        <div class="weui-cells__title">请设置密码</div>
        <div class="weui-cells">
          <div class="weui-cell">
            <div class="weui-cell__bd">
              <input  class="weui-input" @blur="$v.patPassword.$touch()" v-model="patPassword" type="password" placeholder="请输入8-20位密码"/>
            </div>
          </div>
        </div>
        <span class="form-group__message" v-show="showPatPassWord">密码必须是8-20字母和数字组合</span>
        <div class="weui-cells__title">请输入短信验证码</div>
        <div class="weui-cells">
          <div class="weui-cell">
            <div class="weui-cell__bd">
              <input class="weui-input" v-model="captcha" type="number" placeholder="请输入"/>
            </div>
            <div class="weui-cell__ft">
                <button v-show="!(msg>0)" class="weui-vcode-btn" @click="getCode">{{msg}}</button>
                <button v-show="msg>0" class="weui-vcode-btn" @click="getCode">有效期{{msg}}s</button>
            </div>
          </div>
        </div>
      </div>
      <label for="weuiAgree" class="weui-agree">
        <input id="weuiAgree" type="checkbox" v-model="checkbox" class="weui-agree__checkbox"/>
            <span class="weui-agree__text">
                同意<a href="javascript:void(0);">《医药用户协议》</a>
            </span>
      </label>

      <div class="btn" @click="myDetail">
        <a style="background: #30cfd0" href="javascript:;" class="weui-btn weui-btn_primary">下一步</a>
      </div>
    </div>
</template>
<script type="text/ecmascript-6">
    import top from '../../components/app-header.vue'
    import {mainHeightMixin} from '../../lib/mixin'
    import config from '../../lib/config'
    import api from '../../lib/http'
    import { required, between, minLength, maxLength,alphaNum} from 'vuelidate/lib/validators'
    import phone from '../../lib/regex'
    export default{
        components: {
            top
        },
        mixins:['mainHeightMixin'],
        data(){
            return {
              mobile:'',
              patPassword:"",
              captcha:'',
              showError:false,
              checkbox:Boolean,
              showPatPassWord:false,
              cid:'',
                msg:"获取验证码"
            }
        },
      validations: {
        mobile: {
          required,
          phone:phone(1)
        },
        patPassword: {
          required,
          alphaNum,
          minLength:minLength(6)
        }
      },
        mounted(){

        },
        watch:{
            patPassword(){
                if(!/^(?![A-Z]+$)(?![a-z]+$)(?!\d+$)(?!\W+$)\S{8,20}$/g.test(this.patPassword)){
                    console.log(21212121)
                    this.$set(this.$data,'showPatPassWord',true)
                }else {
                    this.$set(this.$data,'showPatPassWord',false)
                }
            }
        },
      methods:{
        getCode(){
            if(this.$v.mobile.$invalid){
                console.log(this.$v)
                this.$set(this.$data,'showError',true)
            }else {
                this.msg = 60;
                var time = setInterval(()=>{
                    this.msg -=1;
                    if(this.msg==0){
                        this.msg='重新获取';
                        clearInterval(time)
                    }
                },1000)
                api("smarthos.captcha.pat.register",{
                    mobile:this.mobile
                }).then(res=>{
                    console.log(res,11111);
                    if(res.succ){
                        this.$set(this.$data,'cid',res.obj.cid);
                        localStorage.setItem('cid',res.obj.cid)
                    }else {
                        this.$weui.alert(res.msg);
                    }
                })
            }


        },
        myDetail(){
          if(this.$v.mobile.$invalid){
            console.log(this.$v)
            this.$set(this.$data,'showError',true)
          }else if(!this.checkbox){
            this.$weui.alert('请先同意协议')
          }else if(this.captcha.length!=4){
            alert('请输入正确的验证码')
          }else {
            api("smarthos.captcha.check",{
              "cid": this.cid,
              "captcha": this.captcha
            }).then(res=>{
              if(res.succ){
                localStorage.setItem('password',this.patPassword)
                localStorage.setItem('captcha',this.captcha)
                this.$router.push({
                  name:'myDetail'
                })
              }else {
                this.$weui.alert(res.msg)
              }
            })

          }

        }
      }
    }
</script>
<style scoped lang='scss'>
    @import '../../common/common.scss';

    .weui-vcode-btn{
      height: auto;
      line-height: 1;
      color: white;
      border: none;
      padding: 5px 3px;
      margin-left: 0;
    }
    .weui-cell__ft{
      background: #30cfd0;
      width: auto;
    }
    .btn{
      width: 100%;
      box-sizing: border-box;
      padding: 80px 30px 40px 30px;
    }
    .form-group__message{
      color: red;
      box-sizing: border-box;
      padding-left: 15px;
      font-size: 12px;
    }
</style>
