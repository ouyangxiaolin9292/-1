#  oxui 全局样式说明文档

##    布局
.container设置为容器：   水平方向居中   宽度100%左右内边距15px高度没有
container-fluid    宽度100%的容器没有外边距内边距15px 上下0px 没高度
##  按钮  ox-btn
 成功  ox-btn-success
 失败  ox-btn-fail
 警告  ox-btn-warning
错误  ox-btn-error
取消  ox-btn-cancel
确认  ox-btn-sure
默认  ox-btn-default
危险  ox-btn-daner
首选  ox-btn-primany
一般信息 ox-dtn-infa
禁止   ox-btn-disable
百搭   ox-btn-normal
暖色   ox-btn-warm
  
  型号
  大  ox-btn-bg
  小  ox-btn-sm
  中  ox-btn-md

  圆角按钮   ox-btn-radius
  ##      渐变色的按钮样式
    成功  ox-btn-success-rgb
 失败  ox-btn-fail-rgb
 警告  ox-btn-warning-rgb
错误  ox-btn-error-rgb
取消  ox-btn-cancel-rgb
确认  ox-btn-sure-rgb
默认  ox-btn-default-rgb
危险  ox-btn-daner-rgb
首选  ox-btn-primany-rgb
一般信息 ox-dtn-infa-rgb
禁止   ox-btn-disable-rgb
百搭   ox-btn-normal-rgb
暖色   ox-btn-warm-rgb

   ### 伪类按钮样式


##  表单


## 滑块


##  选择框

##  表格   .ou-table
.table   表示基础类表格；  必修在table标签使用
.table-column   只有列边框
.table-striped  表示条状表格；表体的偶数行：有一定的背景色
## 表格 .table
.table 表示基础表格；必须在table标签中使用；表示只有列边框的表格
.table-striped 表示条状表格；表体的偶数行；有一定的背景颜色
.table-column 表示半边框样式
.table-hover   表示悬浮表格
.table-condensed  紧缩表格
.table-border  边框表格
.table-inverse  背景为黑色的表格
.table-inverse-strped   黑色条形表格
.table-inverse-hover  黑色悬浮样式    要依赖 .table-inverse   /.table-inverse-striped  
.table-control    表示【控制列】   笃定：  其他列 可以滚动 必修给table的足迹元素添加  二不是 父元素

   ~~~css
   .table-control{
     position:relative;
   }
   .table-control  table>tr>td:last-child{
     position:absolute;
     right:0px;
     min-width:120px;

     text-align:center;
     border-shadow:-5px 4px 6px 1px#ccc;
   }
   /* 选中倒数第2列 解决内容遮蔽问题 */
   .table-control  table>tr>td:last-child(2)::before{
     content:"";
     width:120px;
   }
.table-control>.table-box{
    overflow:auto
}

.table-respansive   移动端表格   可以有横向滚动的效果     .table-responsive需要依靠table的父容器天价
状态表格  给tr加类名
.success   成功
.info  通过
.warming   警告

##  栅格系统

#####  分页  .page
.pagination   实现分页样式   ul  li  a   完成的分页效果
.pagination-bgc     
.pagination-noBgc   表示有背景颜色
.pagination-inverse   表示背景颜色欸黑色的分页
。active  被选中后背景颜色为黑色  字体为白色   .pagination-inverse  基础上
   
   ####   表单类
  .circle-check  圆形选择框  .circle-check  需要给input[type=checkbox]的父元素添加
.square-check  正方形选择框   .square-check  需要给input[type=checkbox]的父元素添加
~~~html
<!-- 示例代码 -->
 <div class="circle-check">
      <input type="checkbox" />
    </div>
    <div class="square-check">
      <input type="checkbox" />
    </div>
~~~


###    滑块   .sliderbar
.sliderbar   表示滑块条
.sliderbar-control   表示控制键
~~~html
 <div class="sliderbar">
         <div class="sliderbar-control"></div>
    </div>
~~~
状态
.sliderbar-success
.sliderbar-info
.sliderbar-primary
sliderbar-crror

   ### 开关    .switch
   .switch   开关样式的选择框    需要给  input[type-checkbox class= switch 才能实现]
    绿色开 input= check    灰色关  input=disable
    状态
    .switch-info  蓝看灰色关
    .switch-dander   红开   灰色关
    

#####  步骤组件  step 

。step-wrap   为外容器   55rem
step-full   没个步骤容器    包含圈先文本
.step    具体具体每步  ipunt[type=checkbox]，  当有checked  时表示当前步骤以完成
,step-circle  表示园
.step-line    线
.step-text    文本
状态
.step-circle-info
.step-circle-success
.step-circle-primary
.step-circle-crror
.step-circle-danger
.step-circle-warm

####  导航  .nav
注意： 只适用于pc端   且只使用静态样式    导航中的样式都是操作li下的a标签
   .nav-tab   表示 tab  样式的导航条   需要依赖.nav
   .nav-pills   胶囊式导航             需要依赖.nav
  .nav-scacked



   .nav-inverse   表示背景为黑色的导航
   .nav-aside   表示侧边导航
   .nav-fixed-top   表示 固定导航在顶部
   .nav-fixed-left   左边栏固定
   .nav-fixed-right   右边栏固定

#####  导航条    .navbar
注意：  兼容移动端 pc  默认样式隐藏
兼容移动端样式设置规则：媒体查询最小宽度；写pc端样式；当小于这个宽度时候；使用浏览器默认样式
网站的导航条；到移动端时候可以折叠 

.navbar  导航条 兼容pc 移动
.navbar-default 给导航条添加样式
.navbar-header 有媒体查询样式；做PC 端和移动端区分； 移动端宽度100%
.collapse  元素隐藏[移动端]
.nav-collapse.collapse 在pc 端【强制】显示
.navbar-nav 表示导航条下导航
.navbar-form 表示导航条中输入框
.navbar-left 让导航在导航条中左浮动【移动端无浮动】
.navbar-right 让导航有又浮动【移动端无浮动效果】
.navbar-toggle 表示显示隐藏列表导航栏，有【右浮动】效果

.navbar-fixed-top 固定顶部导航条
.navbar-inverse 黑色导航条 border-bottom:1px solid black
   .navbar .active  背景颜色黑色  字体白色

 .breadcrumb 表示路径导航；没有基础类  

  - 每个a 添加伪元素； content:"Z/\00a0"


##  规范
1清空所有html默认样式
2：字体：标准14px最大36px最小12px

3：布局  栅格系统    给一个父容器等分多少份
12列：
每个子元素可以占12列中1~12最大12份
col-12占据12份
####   注意
1如果ie7  8  请更换浏览器
2IE7尽量使用  div
nav  div.nav
span   div.span  设置display：inline
3  ie78   不支持 浮动  css3   90%属性


###  表单    form
1：只有表单样式。分为基础样式和可选样式。
2：表单没有进行验证处理  右对验证效果处理  statice  状态
3： 表单验证要用就是js   正规完成    不能写新的规定
.form-group 表示表单组件
form-control   表单控件
.form-label    表示input 的信息值能应用label中

####  可选项表单
.form-inline   表示横向表单
.form-horizontal纵向表单


#### 表单控件
.form-check   选择项
.form-check-item   表示多选项
。check-content   表示  选择的文本描述

.from-group  表单组建；默认宽度100%
.from-inline  横向的表单；  display ：inline-block
.form-control 表示表单控件
.examInputEmail  邮箱
.examInputPassword 密码
.examInputUsername  用户名
.select  选择框
.selectFile 选择文件
.inputSubmit  按钮提交  ???
.help-block 文件路径提示信息
.input-group 输入框组件
    - input-group-addcon

   - input-group-add  加
   - input-group-decaline 减
   - input-gropu-addIcon 添加图标

水平排列表单
.form-horizontal 可以是Lable 水平排列

内敛单选多选款 .checkbox-inline
多选：
.inlineCheckbox
单选  .inlineRadioOption

不带文本的选择框  .checkbox
正方形  .blankCheckbox
原型：  .blackRadio

静态控件
control-label
form-control-static

禁止输入 #disableInput

校验样式
has-success 成功  字体 边框 绿色
has-warning  警告    黄色 
has-error 失败  红色

 尺寸
 .input-lg 大输入框
 .input-sm 小输入框



#####  栅格系统    .col
是横向布局
如果父容器：不适用row   那么自己清除浮动；计算父容器高度


####  row
将row容器 分为12分
####   屏幕
.col-xs-xx   768以下
.col-sm-xxx  768~992
.col-md-xx     992~1200
col-lg-xx 1200以上




#### 分的份数    小数点7位
1： 8.33333333%
2； 16.6666667%
3:  25%
4;  33.3333333%
5:  41.6666667%
6:  50%
7:  58.3333333%
8:  66.6666667%
9:  75%
10: 83.3333333%
11: 91.6666667% 
12:  100%



##### 列偏移 

通过改变position：relation    left   实现偏移
-xx表示1~12
.col-xs-offset-xx
.col-sm-offset-xx
.col-md-offset-xx
.col-lg-offset-xx

#####  排列
.col-xs-pull-xx  相对元素左边多远