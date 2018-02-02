<template>
    <div>
        <div id="comment-list" class="comment-list">
            <!--提交的留言表单-->
            <form class="new-comment">
                <nuxt-link class="avatar" to="/u/123">
                    <img src="../assets/img/default-avatar.jpg" alt="">
                </nuxt-link>
                <textarea @focus="send=true" placeholder="写下你的评论" v-model="value">

                </textarea>
                <transition :duration="200" name="fade">
                    <div v-if="send" class="write-function-block clearfix">
                        <div class="emoji-modal-wrap">
                            <a class="emoji" @click="showEmoji=!showEmoji">
                                <i class="fa fa-smile-o"></i>
                            </a>
                            <transition :duration="200" name="fade">
                                <div v-if="showEmoji" class="emoji-modal arrow-up">
                                    <vue-emoji @select="selectEmoji"></vue-emoji>
                                </div>
                            </transition>
                        </div>
                        <div class="hint">
                            Ctrl+Enter 发表
                        </div>
                        <a class="btn btn-send" href="javascript:void (0)" @click="sendData">发送</a>
                        <a @click="send=false" class="cancel" href="javascript:void (0)">取消</a>
                    </div>
                </transition>
            </form>
        </div>
    </div>
</template>
<script>
    import vueEmoji from '~/components/vueEmoji'
    export default {
        name:'myComment',
        data(){
            return{
                send:false,
                showEmoji:false,
                value:'',
            }
        },
        methods:{
            selectEmoji:function (code) {
                this.showEmoji = false;
                this.value += code
            },
            sendData:function () {
                console.log('发送value值得数据给后端')
            }
        },
        components:{
            vueEmoji
        }
    }
</script>
<style>
    .fade-enter-active,.fade-leave-active {
        opacity: 1;
        transition: .3s;
        -webkit-transition: .3s
    }

    .fade-enter,.fade-leave-to {
        opacity: 0;
        transform: translate3d(0,-5%,0);
        -webkit-transform: translate3d(0,-5%,0);
        transition: .3s;
        -webkit-transition: .3s
    }
    .note .post .comment-list{
        padding-top: 20px;
        margin-bottom: 200px;
    }
    .note .post .comment-list .new-comment {
        position: relative;
        margin-left: 48px;
        margin-bottom: 20px;
    }
    .note .post .comment-list .avatar{
        width: 38px;
        height: 38px;
        display: inline-block;
        margin-right: 5px;
    }
    .note .post .comment-list .new-comment .avatar{
        position: absolute;
        left: -48px;
    }
    .note .post .comment-list .new-comment textarea{
        width: 100%;
        height: 80px;
        padding: 10px 15px;
        border: 1px solid #ccc;
        display: inline-block;
        vertical-align: top;
        outline-style: none;
        resize: none;
        font-size: 13px;
        background-color: #f8f8f8;
        position: relative;
        z-index: 999;
    }
    .note .post .comment-list .new-comment .emoji-modal-wrap{
        position: relative;
    }
    .note .post .comment-list .new-comment .emoji{
        float: left;
        margin-top: 14px;
    }
    .note .post .comment-list .new-comment .emoji i{
        color: #969696;
        font-size: 22px;
    }
    .note .post .comment-list .new-comment .emoji i:hover{
        color: #333!important;
    }
    .note .post .comment-list .new-comment .hint{
        float: left;
        margin: 16px 0 0 15px;
        font-size: 13px;
        color: #969696;
    }
    .note .post .comment-list .new-comment .cancel{
        float: right;
        font-size: 16px;
        margin: 18px 30px 0 0;
        color: #969696!important;
    }
    .note .post .comment-list .new-comment .cancel:hover{
        color: #333!important;
    }
    .note .post .comment-list .new-comment .btn-send{
        float: right;
        width: 78px;
        padding: 8px 18px;
        margin: 10px 0;
        font-size: 16px;
        background: #42c02e;
        border-radius: 20px;
        color: #fff!important;
        box-shadow: none;
    }
    .note .post .comment-list .new-comment .btn-send:hover{
        background: #3db922;
    }
    .note .post .comment-list .new-comment .emoji-modal-wrap .emoji-modal{
        position: absolute;
        top: 50px;
        left: -48px;
        width: 402px;
        height: 208px;
        padding: 10px;
        border: 1px solid #d9d9d9;
        border-radius: 4px;
        box-shadow: 0 5px 25px rgba(0,0,0,.1);
        z-index: 10001;
    }
    .arrow-up:after{
        content: "";
        display: inline-block;
        position: absolute;
        left: 50px;
        top: -1px;
        border-left: 1px solid #d9d9d9;
        border-top: 1px solid #d9d9d9;
        background: #fff;
        width: 10px;
        height: 10px;
        transform: translate3d(0,-50%,0) rotate(45deg);
    }
</style>