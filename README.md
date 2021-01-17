# 萌新博客
有不懂的标签用谷歌搜索
```
MDN 关键字
```
永远不要让图片变形！
## 12.21

学会了上传代码到github
时间线跃迁 git reset --hard 6位标识符

## 12.22

1. WWW的发明与壮大
2. 了解HTML是什么
3. 掌握CRM学习方法
 * Copy
 * Running
 * Modify
 * 先抄后运再修改
4. html的四种标签
  ```html
    <!DOCTYPE html></html>
    <div id="title">???</div>
    <head>!!!</head>
    <div id=不用反斜杠>
  ```
5. 调试
  * vs code
  * webstorm
  * 在线调试 validator.w3.org

## 12.23

1. 学习html各个属性的用法
  * 不到万不得已,千万不要用id,因为id标签不会报错
  * id的作用,js可以直接获取id
  * id不能命名为全局属性名,即window.之后的所有单词
  * tabintex=0 是tab最后访问的地方 -1是tab不访问的地方
  * css可以在F12的style界面直接调试
  * title是鼠标指到之处浮动的小窗
2. 学习css内容标签
  * ol+li //ordered list + list item 有序列表
  * ul+li //unordered list + list item 无序列表
  * dl+dt+dd //description list+term+data 标题与介绍
  * pre // 使得多个空格能显示
  * * html的特点：多个空格/回车会合并成一个空格/回车
  * code // 里面的字符等宽
  * hr //分割线
  * br //break 换行
  * a //anchor 多用于超链接 
    ```html
     <a href="link">text</a>
     <a href="target="_blank</a>表示在新窗口打开
     ```
  * em //emphasis 语气强调
  * strong // 内容本身的重要性
  * q //quote 引用 没效果
  * blockquote // 换行引用

## 12.24
1. yarn global http-server
  * http-server . -c-1 -c代表缓存功能 -1代表不用这样做
2. 永远不要双击打开html 这样调试环境不同
3. yarn global add parcel时 因为node已经到达10.0,需要自行寻找8.0的parcel
  * 然后有bug,选择用http-server
4. a标签的download很多浏览器不支持
5. rel=noopener 为了防止一个bug 目前还没学
6. a的href的取值有9种
  * https协议,http协议,以及无协议的//,无协议优先选https,写链接时优先写//
  * id,用于跳转到指定标签href写#xxx,要跳转的标签id写xxx
```html
        <a href="#999">跳转</a>
        <p id="999">990</p>
```
  * 路径,绝对和相对路径均可.
  * 伪协议
  * javascript:代码
  * * 特殊用法:javascript:;使超链接点击后什么事都不会发生
  * mailto:邮箱
  * tel:手机号  面试时用来给面试官直接拨号给你
7. a的target的取值
  * _blank 新窗口打开
  * _self 当前页面打开
  * _top 使用此值后,在里面可以引用一个iframe页面
  * _parent 在此页面的上一层iframe页面打开链接
  * id,打开一个唯一id的页面,若其它链接id也相同,则会在此页面替换链接,想查该页面的id可以通过Console输入window.name
8. iframe 在当前窗口创建一个嵌入式页面
9. table 只有三个标签
  * thead
  * tbody
  * tfoot
  * 这三个标签里面可以有
```
  th(head组成一行,加粗)
  tr(row能组成一列)
  td(date组成一行，不粗)
```
  * table-layout:样式,auto根据内容调整宽度,fixed尽量平均宽度
  * border-collapse:使得格子之间没有缝隙
  * border-spacing:0也能达到同样效果。此值代表各格间距
10. img
  * src即图片地址
  * alt是当src图片加载失败时显示的内容
  * onload,onerror,监听图片加载
  * * 
     ```
     id.onload = function(){
       console.log("加载成功");
     }
     id.onerror = function(){
       console.log("加载失败")
     };
     即可计数成功失败次数
     ```
  * max-width:100% 响应式,使得图片在任何尺寸屏幕都显示全
11. form
  * action属性控制请求哪个页面
  * method属性控制用get还是post请求(以后会讲)
  * autocomplete自动填充
  * target 同a标签
  ```html
  <input type="submit" value="搞起">
  <button type="submit">搞起</button>
  ```
  区别在于,button里面还可以加标签
  * form里面必须有一个含有type="submit"的属性,如果没有,则会给一个没有属性的button添加submit
  * form里的input一定要有name
12. input
  * text
  * color
  * password
  * radio单选按钮,想让两个单选按钮互斥,就使其在同一组
  ```html
  <input name=class type="radio">1
  <input name=class type="radio">2
  ```
  * checkbox多选按钮
  * file选择文件,想多选则在后面加上multiple
  ```html
  <input type="file" multiple>
  ```
  * hidden隐藏
  * textarea多行输入框默认能拖动,不让拖的属性如下
  ```html
  <textarea style="resize: none;">
  ```
  * select就是下拉选单
  ```html
  <select name="请选择日期" id="">
  <option value="1">大年初一</option>
  <option value="2">2</option>
  </select>
  ```
  * onchange 
  * onfocus 把鼠标指在该处
  * onblur 把鼠标从该处挪走
## 12.24
  vscode输入多行的办法
  选中想输入的多行
  ctrl+shift+P
  输入emmet wrap
  在框中输入ul>li*即可获得如下效果
  ul>表示用一个ul框柱选中部分
  *表示每一条选中都被li框柱
  ```html
      <ul>
        <li>司马炎</li>
        <li>杨骏</li>
        <li>司马衷</li>
        <li>贾南风</li>
        <li>司马亮</li>
        <li>司马玮</li>
        <li>司马繇</li>
    </ul>
  ```
## 12.28
  * 重温如何克服拖延症,然后继续做html
  * 学习正则表达式
  * meta:vp的完整内容
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0, user-scalable=no">

```

## 2021.1.4
>工作荒废了几乎一星期，重新起航！
  * css2.1使用最广泛 css3正在使用,每个模块独立升级
  * caniuse.com 输入特性名 就能知道各个浏览器支持什么特性
  * css只有两种语法
```
  选择器 {
  属性名: 属性值;
  /*注释*/
  }
```
```
  @charset "UTF-8"; //指定文件编码
  @import url(2.css); //导入css文件
  @media (min-width: 100px) and (max-width: 200px) {
  语法一
  } //媒体查询，以后会讲
```
  * 如何调试CSS 
  1. webstorm
  2. F12看该标签
  3. 最强方法 Border调试法！
```
  怀疑某个元素有问题
  就给这个元素加 border
  border 没出现？说明选择器错了或者语法错了
  border 出现了？看看边界是否符合预期
  bug 解决了才可以把  border 删掉
```
  * 在哪查css资料呢
  1. mdn 样式
  2. css trick
  3. 张鑫旭的博客
***
  * 在哪练习（抄）呢
  1. PSD
  * Freepik 搜索 PSD web
  * 365PSD 里的 UI 套件还行
  2. 效果图（不提供下载）
  * dribbble.com 顶级设计师社区
  3. 商业网站
  * 直接模仿你常去的网站
***
  >外包公司的缺点，你做的都是重复工作。不能呆超过一年半，否则无法提升。
  * margin默认能多宽有多宽
  * 学精JS好过学精CSS
## 1.5
  >盒模型分两种，content-box和border-box
  * 内容盒的宽度和设定的一样
  * 边框盒的宽度=borer+padding+内容
***
  * 孩子之间的margin会合并
  * 外边距合并只在上下存在
  * border-radius:50% 就是圆形
***
## 1.7
  1. float布局，IE用的了解一下就行，以后大概用不上了。
  * 如果图片下面有颜色溢出，加一行vertiacl-align:top;
  * border调试可能会干扰位置，可以换成outline。
  * 居中方法margin-left:auto; margin-right:auto;
  * 如果需要平均布局，会需要用到负margin。负margin不会换行。
***
## 1.9
  1. flex容器由两种写法
```css
.container{
  display: flex; /*快捷输入 d:f + tab*/
}/*这个会另起一行*/
```
```css
.container{
   display: inline-flex;
}/*这个不会另起一行*/
```
  * flex-direction:row; 流向横/反横/纵/反纵
  * flex-wrap: wrap; 是否换行wrap是/nowrap否
  * justify-content: 主轴（默认为横）对齐方式
  * align-items: 副轴（默认为纵）对齐方式
***
## 1.10
  1. grid布局,快淘汰了
## 1.11
  1. 学习css层级
  * float属性的div在普通div的上方
  2. position: static;默认属性 什么都不改，所以也不用写出来
  3. position: relative;属性
  * z-index:1 表示比0高一层
  4. position: absolute;属性<br>
 <span style="color:red;">会找第一个不是static的祖先标签进行匹配，不是只找relative</span>
> white-space:nowrap; 文字内容不准换行，通常用于button按钮

```css
button span{
  display: none; /* 内容不显示 */
}
button:hover span{
  display: inline-block; /* 鼠标挪过去才显示 */
}
```

  * F12-style-hov-hov打钩 就可以看鼠标悬停内容
  5. position:fix;相对于视口定位，具体来说对于iframe标签，常用语回到顶部按钮。
  * fix不要和transform混用，会出现问题。
  * fix别用在移动端，全是问题。
  6. position: sticky;窗口下滑时总有一行悬浮在最上方，意为粘滞。
  7. z-index: 层级从上到下为
```
99
...
1
0
-1
...
但是不能跑到html后面
```
***
## 1.17
  * 打开控制台按ESC，点击console旁边的三点，选择rendering，给paint flashing打钩。就可以看渲染过程。闪烁一次代表渲染一次。
  * ctrl+shift+L 饥人谷js代码格式化
  * csstriggers.com 写了不同浏览器的渲染方式
***
渲染原理
1. HTML构建HTML树
2. CSS构建CSS树
3. 合并成一颗渲染树
4. Layout-Paint-Compose依次进行
***
transition
```css
#heart{
  margin:100px;
  position:relative;
  display: inline-block;
  transition: all .5s;
}
#heart:hover{
  transform:scale(1.5);
}
```
***
animation
```css
#heart{
  margin:100px;
  position:relative;
  display: inline-block;
  animation: heart 1s alternate infinite;
}
#heart:hover{
  from{
    transform:scale(1.0);
  }
  to{
    transform:scale(2.0);
  }
}
```
***
个人感觉animation更灵活一些
***
### HTTP部分
127.0.0.1 表示自己<br>
localhost 表示通过host指向自己<br>
0.0.0.0 不指向任何设备<br>
node.js
* ``这种引号里面可以用回车
* ''这种引号必须写\n才能回车

vscode ctrl+/ 一键注释<br>
node server.js 8888 运行js服务器