<template>
    <div class="sign">
        <div class="logo">
            <nuxt-link to="/">
                <img src="../assets/img/logo.png" alt="">
            </nuxt-link>
        </div>
        <!--注册表单-->
        <div class="main">
            <div class="title">
                <h4>
                    <nuxt-link to="/sign-in">
                        登录
                    </nuxt-link>
                    <b>·</b>
                    <nuxt-link class="active" to="/sign-up">
                        注册
                    </nuxt-link>
                </h4>
            </div>
            <div class="js-sign-up">
                <form method="post">
                    <div class="input-prepend">
                        <input class="top-radius" type="text" value="" placeholder="手机号或邮箱">
                        <i class="fa fa-user"></i>
                    </div>
                    <div class="input-prepend">
                        <input type="text" value="" placeholder="手机号">
                        <i class="fa fa-mobile-phone"></i>
                    </div>
                    <div class="input-prepend ssm">
                        <input type="text" name="" value="" placeholder="手机验证码">
                        <i class="fa fa-shield"></i>
                        <a class="send-ssm btn btn-success">发送验证码</a>
                    </div>
                    <div class="input-prepend">
                        <input class="bottom-radius" type="password" value="" placeholder="密码">
                        <i class="fa fa-lock"></i>
                    </div>
                    <input class="btn btn-success sign-up-btn" type="button" value="注册">
                    <p class="sign-up-msg">
                        点击 “注册” 即表示您同意并愿意遵守简书<br>
                        用户协议 和 隐私政策 。
                    </p>
                </form>
                <div class="more-sign">
                    <p>社交账户登录</p>
                    <ul>
                        <li class="weixin">
                            <a href="#">
                                <i class="fa fa-weibo"></i>
                            </a>
                        </li>
                        <li class="qq">
                            <a href="#">
                                <i class="fa fa-weixin"></i>
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    import '~/assets/css/sign.css'
    export default{
        layout:'sign',//指明当前页面所使用的默认模板是layouts文件夹下的sign.vue
        head(){
            return{
                title:'注册-简书',
                meta:[
                    {hide:'description',name:'description',content:'注册页面'}
                ]
            }
        }
    }
</script>