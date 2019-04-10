<template>
    <div id="app">
        <Header></Header>
        <div class="sudoku_row"  >
            <div class="sudoku_item " v-for="(sudoku,index) in sudokus" :key="index" >
                {{sudoku.name}}
            </div>
        </div>
        <el-card class="box-card" shadow="always">
            <div slot="header" class="clearfix">
                <span>最新资讯</span>
                <el-button style="float: right; padding: 3px 0" type="text">更多</el-button>
            </div>
            <div v-for="(index,item) in zixun" :key="item.id" class="text item">
                {{index.text}}
            </div>
        </el-card>
        <div class="body">
            <div class="btn">
                <el-button type="success" class="button">科目一考试</el-button>
                <el-button type="danger" class="button">科目四考试</el-button>
            </div>
        </div>
    </div>
</template>
<script>
import Header from "@/components/Header";
export default {
    components:{Header},
    name: 'sudoku',
    data() {  
        return {  
        sudokus:[{id:0,name:'驾考资讯'},
                 {id:1,name:'驾考宝典'},
                 {id:2,name:'驾考视频'},
                 {id:3,name:'交通标识'},
                 {id:4,name:'科目一考试'},
                 {id:5,name:'科目四考试'},
                 {id:6,name:'科目二学习'},
                 {id:7,name:'科目三学习'}
                ],
        zixun:[{id:0,text:'杭州最新驾考资讯杭州最新驾考资讯杭州最新驾考资讯杭州最新驾考资讯'},
               {id:1,text:'杭州最新驾考资讯杭州最新驾考资讯杭州最新驾考资讯杭州最新驾考资讯'},
              ]
        };  
    },
}
</script>
<style>
    body{
        background: #ddd;
    }
    .sudoku_row{
        display: flex;
        align-items: center;
        width:100%;
        flex-wrap: wrap;
    }
    .sudoku_item{
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        width:25%;
        height: 120px;
        padding-top: 10px;
        padding-bottom: 10px;
        font-size: 30px;
        background: #666;
        color: #fff;
        border: 1px solid #999;
    }
    .text {
        font-size: 14px;
    }

    .item {
        width: 100%;
        height: 200px;
        margin-bottom: 18px;
        border-bottom: 1px solid #ddd;
    }

    .clearfix:before,
    .clearfix:after {
        display: table;
        content: "";
    }
    .clearfix:after {
        clear: both
    }

    .box-card {
        width: 98%;
        margin: 30px auto;
    }
    .body{
        width: 100%;
        height: auto;
        background: #fff;
    }
    .btn{
        width: 100%;
        height: 150px;
        display: flex;
        flex-direction: row;
    }
    .button{
        width: 47%;
        height: 80%;
        margin: 11px auto;
    }
</style>