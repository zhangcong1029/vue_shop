<template>
    <div class="login_container">
        <div class="login_box">
            <!-- 头像区域 -->
            <div class="login_avatar">
                <img src="../assets/logo.png" alt="">
            </div>
            <!-- 登录表单区域 -->
            <el-form :model="loginForm" label-width="0px" class="login_from">
            <el-form-item>
            <el-input prefix-icon="iconfont icon-user" v-model="loginForm.username"></el-input>
            </el-form-item>
            <el-form-item>
            <el-input prefix-icon="iconfont icon-3702mima" v-model="loginForm.password"></el-input>
            </el-form-item>
            <!-- 密码区域 -->
            <el-form-item class="btns">
            <el-button type="primary">登录</el-button>
            <el-button type="info">重置</el-button>
            </el-form-item>
            </el-form>
        </div>
        
    </div>
</template>
<script>
export default {
    name:'login',
    data () {
        return {
            loginForm:{
                username:'admin',
            password:'123456'
            }
        };
    },
    methods:{
    
    }
}
</script>
<style scoped lang="less">
    .login_container{
        background: #2b4b6b;
    height: 100%;
    .login_box{
        width: 450px;
        height: 300px;
        background: #fff;
        border-radius: 3px;
        position: absolute;
        left: 50%;
        top: 50%;
        transform: translate(-50%,-50%);
        .login_avatar{
            width: 130px;
            height: 130px;
            background: #fff;
            border-radius: 50%;
            position: absolute;
            left: 50%;
            top:0;
            transform: translate(-50%,-50%);
            img{
                width: 100%;
                border-radius: 50%;
            }
        }
    }
    }
    .login_from{
        position: absolute;
        left: 0;
        bottom: 0;
        width: 100%;
       box-sizing: border-box;
        padding: 0 20px;
        .btns{
            display: flex;
            justify-content: flex-end;
        }
    }
</style>