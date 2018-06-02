<template>
  <div id="app">
    <background></background>
    <el-container>
        <el-header>
          <el-row>
            <el-col :span="24"><div class="nav">TodoList</div></el-col>
          </el-row>
        </el-header>
        <el-main>
        <!-- 输入部分 -->
          <el-row>
            <el-col :span="24">
              <div class="list">
              <form @submit='add' action='http://localhost:8080/'>
                <el-input v-model="input" placeholder="TodoList"  suffix-icon="el-icon-edit" ></el-input>
              </form>
              <!-- 表单提交到当前页 -->
              <iframe id="rfFrame" name="rfFrame" src="about:blank" style="display:none;"></iframe>
              </div>
            </el-col>
          </el-row>
          <!-- 显示部分    正在进行-->  
          <el-row>
            <el-col :span="24">
              <div class='do'>
                <el-card class="box-card">
                  <div slot="header" class="clearfix">
                    <span>正在进行</span>
                    <el-button type="success" round size='small' class='number'>{{list.length}}</el-button>
                  </div>
                  <div v-for="item in list">
                  <!-- 绑定事件时有问题 -->
                     <!-- <el-checkbox v-model="item.completed" @click.native='complete(item)'></el-checkbox> -->
                     <input type="checkbox" v-model='item.completed' @click='complete(item)'/>
                     <el-input class='text' v-model='item.text' :disabled='editing' @dblclick.native='edit' @keyup.native.enter='save'></el-input>
                     <i class="el-icon-delete delete" @click='removeDoing(item.id)'></i>
                  </div>
                </el-card>
              </div>
            </el-col>
          </el-row>
          <!-- 显示部分    已完成 -->
          <el-row>
            <el-col :span="24">
              <div class='do'>
                <el-card class="box-card">
                  <div slot="header" class="clearfix">
                    <span>已完成</span>
                    <el-button type="success" round size='small' class='number'>{{completedItems.length}}</el-button>
                  </div>
                  <div v-for='item in completedItems'>
                     <input type="checkbox" v-model='item.completed' @click='uncomplete(item)'/>
                     <el-input class='text' :class='{completestyle:item.completed}' v-model='item.text' :readonly='editing' @dblclick.native='edit' @keyup.native.enter='save'></el-input>
                     <i class="el-icon-delete delete" @click='removeDone(item.id)'></i>
                  </div>
                </el-card>
              </div>
            </el-col>
          </el-row>
        </el-main>
    </el-container>
  </div>
</template>

<script>
import Bg from './components/bg.vue'
export default {
  name: 'app',
  components:{
    background: Bg
  },
  data () {
    return {
      input: '',
      list:[],
      editing:true,
      // 保存所有完成的所有项
      completedItems:[]
    }
  },
  methods:{
    //提交时获取输入数据
    add(){
      document.forms[0].target="rfFrame";
      //如果输入内容不为空则添加
      if(!this.input){
        return;
      }
      //如果内容重复则不添加
      var len = this.list.length;
      for(var i=0;i<len;i++){
        if(this.input == this.list[i].text){
          this.input = '';
          return;
        }
      }
      this.list.push({
        id:Math.random(),
        text:this.input,
        completed:false
      });
      this.input = '';     
    },
    //双击变为可编辑状态
    edit(){
      this.editing = false;
    },
    //回车保存改变后的值
    save(){
      this.editing = true;
    },
    //删除正在进行对应条目
    removeDoing(id){
      var len = this.list.length;
      for(var i=0;i<len;i++){
        if(id === this.list[i].id){
          this.list.splice(i,1);         
          break;
        }
      }
    },
    // 删除已完成对应条目
    removeDone(id){
      var len = this.completedItems.length;
      for(var i=0;i<len;i++){
        if(id === this.completedItems[i].id){
          this.completedItems.splice(i,1);
          break;
        }
      }
    },
    //完成时添加到另一栏
    complete(task){
      //刚开始点击时为false，点击后才变为true
     if(!task.completed){
      this.completedItems.push(task);
      this.removeDoing(task.id);
     }
    },
    //未完成时又回到真在进行那栏
    uncomplete(task){
      if(task.completed){
        this.list.push(task);
        this.removeDone(task.id);
      }
    }
  }
}
</script>

<style>
   .nav{
    text-align: center;
    background-color: #cdcdcd;
    color:#323232;
    font-size: 1.5rem;
    font-weight: bold;
    padding: 1rem 0;
    border-radius: 1rem;
   }
   .do{
    padding:1rem 1rem;
    color:white;
    font-size:1.5rem;
   }
   .do .number{
    float: right;
   }
   .do .delete{
      color:red;
      float:right;
      cursor: pointer;
   }
   .do .text{
    width:700px;
    margin-left: 50px;
   }
   .do .el-input__inner {
    border:none;
    color:black!important;
   }
   .completestyle .el-input__inner{
    text-decoration:line-through;
    color:#a19f9f!important;
   }
</style>
