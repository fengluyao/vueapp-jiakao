<template>
    <el-container>
        <el-header class="header">
            <el-row :gutter="20">
                <el-col :span="6" :offset="1">
                    <div class="grid-content">
                        <img src="https://m.ixbest.com/addons/zjhj_mall/core/web/uploads/image/b9/b987f74259e0c263017481bddf6a8df998d72801.jpg" alt="" class="logo" @click="aclick()">    
                    </div>
                </el-col>
                <el-col :span="10">
                    <div class="grid-content title" v-text="title"></div>
                </el-col>
                <el-col :span="3">
                    <div class="grid-content">
                        <img src="https://m.ixbest.com/addons/zjhj_mall/core/web/uploads/image/54/541dd6bca07899f7f6621edb342bd398be6b511e.jpg" alt="" class="right">
                    </div>
                </el-col>
                <el-col :span="4">
                    <div class="grid-content">
                        <img src="https://m.ixbest.com/addons/zjhj_mall/core/web/uploads/image/0b/0bdb80263039e523e0fb1767cb6f25dcd6b33e0b.jpg" alt="" class="right">
                    </div>
                </el-col>
            </el-row>
        </el-header>
    </el-container>
</template>
<script>
export default {
    data(){
        return {
            title : "驾考神器"
        }
    },
    methods:{
        aclick(){
            this.$router.push({name:'HelloWorld'});
        }
    }
}
</script>
<style>
    .header{
        background: #20AE88;
        height: 200px !important;
    }
    .grid-content {
        border-radius: 10px;
        height: 200px;
    }
    .logo{
        width:auto;
        height:90%;
        margin-top: 3%;
    }
    .right{
        width: auto;
        height: 100%;
    }
    .title{
        color: #fff;
        font-size: 100px;
        font-weight: bold;
        text-align: center;
        line-height: 200px;
    }
</style>