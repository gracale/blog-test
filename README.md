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
  * * 这三个标签里面可以有th(table head组成一行),tr(table row能组成一列),td(table date加粗效果)
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