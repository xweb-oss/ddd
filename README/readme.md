 15. 箭头函数    ...扩展符号  class  promise   结构赋值    结构参数     长字符串模板    块级作用域let和const  
    谈谈箭头函数 有什么特点  ()=>{}
      没有自身的this    借用函数外部的this
    this和调用的位置有关，和声明的位置无关

 Promise 对象用于异步操作，它表示一个尚未完成且预计在未来完成的异步操作。有三种状态，pending  reject  resolve
    在使用的时 ：Promise构造函数会接受一个 函数  作为参数，该函数的 两个参数 分别是 resolve和 reject。它们是两个函数

17. vue中异步函数async和await的用法  和 promise 不同
     1. 简洁了代码，不像 promise 一样需要then ，
     2. promise 中不能自定义使用 try/catch进行错误的捕获 ，在 async/await 可以像同步一样处理代码错误信息。

    a. 也就是说async函数会隐试的返回一个Promise对象。
    b. async 函数中 return 的值  就是Promise对象中resolve的值；
    案例   ：见  项目 g/app/type-detail.vue

data为什么是函数（return）: 如果单纯的对象，相当于所有组件共用一个 data ,这样改一个全多改了 。 
是函数的话，相当于给每个组件实例一个私密的空间，各自负责自己的模块，不会产生冲突。
 
$nextTick ：当修改了data的值后马上获取这个dom 元素的值是获取不到的，需要用到 $nextTick 这个回调 跟新到新的dom后在获取

虚拟dom  : 用javascript模拟dom树，并渲染 ，然后和老的 dom树进行对比，得到的差役渲染到 dom 树上。
          （ 虚拟dom 渲染速度快点, 实际dom渲染之前要先清除 。）
宏任务包括有：setTimeOut、setInterval、setImmediate、I/O、用户交互操作，UI渲染
微任务包括有：Promise(重点)、process.nextTick(nodejs)、Object.observe(不推荐使用) 
（js引擎发起的叫微观任务 ）

1. h5的新特性：audio  video 本地存储  地理定位  表单控件. canvas 
    css3 新特性
    圆角  阴影  背景渐变  弹性盒布局  过渡  动画  2D/3D转换  媒体查询  border-image

3. 闭包，能调用其它函数变量的函数，
   特点，函数嵌套函数，锁内存，不会被被回收   
   缺点: 不适当的使用，会造成内存泄漏。

14. 原型链 
  原型链：简单的理解就是查找属性 ，自己找不到，去上一层查找。在找不到，再去上一层找

4. 深拷贝和浅拷贝，数据类型分为二类，直类型，引用类型，他们存在不同的空间栈和堆中，而深浅拷贝是针对引用类型的，浅拷贝拷贝引用类型的内存地址指针，指向同一个对像，深拷贝会在堆内存中从新开劈一个内存空间，生成了二个不同的对象

4. w3c规范  ：标签小写， 属性值要用双引号，标签合理嵌套，图片要带alt属性         
 能够书写良好的代码，能够兼容主流浏览器（IE9）    =====对搜索引擎友好。
web标准 ：结构，表现 ，行为

5. src 的内容，是页面必不可少的一部分，是引入。href 的内容，是与该页面有关联，是引用。 
   href 表示超文本引用（hypertext reference），在 link和a 等元素上使用。src 表示来源地址，在 img、script、iframe 等元素上

6. vue的优化
    2.Keepalive 缓存，懒加载，将代码重复封装放到get 里面
    1.给props 传直不要传对象，因为对象可变的，会影响性能。
    3遍历的时候，Key 属性尽量不用数组的下标，因为数组变化了，key 直会发生变化，会重新污染页面，

7. 创建：beforeCreate 创建前     el data message 全部为undefind
        created:	创建        el undefind   data  message有值
        挂载：beforeMount;挂载前
        moutned;挂载
        更新：beforeUpdata;更新前
        updataed;更新
        销毁：beforeDestroy；销毁前
        destroyed：销毁

8. 指令的区别  v-if  v-show对比    v-text v-html对比
    a,v-text是用于操作纯文本 ，可以简写为{{}},并且支持逻辑运算。   注：vue中有个指令叫做 v-once 可以通过v-once与v-text结合，实现仅执行一次性的插值
    b,v-html用于输出html 将当作html标签解析后输出。
    c,v-if显示隐藏是将dom元素整个添加或删除  v-show隐藏则是为该元素添加css--display:none，dom元素还在。

9. get post区别
   get   显示在地址栏中  长度有限制  明文传输入 
   post 显示在请求体中  不是明文传输入

12. em和rem共同点：相对于字体大小变化，不是相对于宽高，rem相对于根节点，em相对父元素而言，动态设置字体大小 

13. this的四种指向 
      a.如果是一般函数,this指向全局对象window;
      b.在严格模式下"use strict",为undefined.
      c.对象的方法里调用,this指向调用该方法的对象.
      d.构造函数里的this,指向创建出来的实例

Ajax其核心有 JavaScript、XMLHTTPRequest、DOM对象组成，通过XmlHttpRequest对象来向服务器发异步请求，从服务器获得数据， 然后用JavaScript来操作DOM而更新页面。

22. vue数据双向绑定的原理。
实现一个监听器Observer，用来劫持并监听对象中所有属性的变化，然后通知订阅者。由于vue中是通过v-model，v-on等指令来实现驱动试图的，而订阅者不能解析指令，所以需要一个解析式将指令解析成相对行的函数，订阅者执行这个函数，更新试图

消息的发送者（称为发布者）不会将消息直接发送给特定的接收者（称为订阅者）。

9.  全局守卫：router.beforEach(fun)       router.afterEach(fun)  router.beforeResolve
    独享守卫：    只在进入到某个指定的路由时才会触发该函数  例如:
 *  {path:"/home",component:xxx,beforeEnter:(to,from,next) =>{}}
    内部守卫：    beforeRouteEnter(to,from,next){} //在进入到某个会加载当前组件的路由时
                 beforRouterUpdate    beforeRouterLevel

10. css hack   及时针对不同的浏览器写不同的 css 叫做hack       bfc  :格式上下文

21.  如何区分  宿主对象  内置对象  本地对象  分别有哪些? 
本地对象为array obj regexp 等可以new实例化
内置对象为gload Math等不可以实例化的
宿主对象为浏览器自带的ducument，window等

vue 好处  特性   1. 轻量级的框架 数据双向绑定 指令  （v-text：操作纯文本 ，v-html 解读html标签）

0000000. vuex的架构的原理。
     将数据集中在state中进行管理，视图层通过计算属性获取state中的值，视图层用户的行为会产生action,通过this.$store.dispatch分发action，连接到store中的actions，通过store.commit触发mutation,然后修改state，最后vue会重新刷新视图

     Getter： 对state中的数据派生出一些状态，例如对数据进行过滤。
     Mutation：
        更改 Vuex 的 store 中的状态的唯一方法是提交 mutation。
        一条重要的原则就是要记住 mutation 必须是同步函数。

     Action 提交的是 mutation，而不是直接变更状态。Action 可以包含任意异步操作

15. **由于动态路由也是传递params的，所以在 this.$router.push() 方法中path不能和params一起使用，否则params将无效。需要用name来指定页面。name匹配  query和params,  而path只能匹配query
**query传参的参数会带在url后边展示在地址栏，params传参的参数不会展示到地址栏。需要注意的是接收参数的时候是route而不是router。
*****this.$router.push({name:'list', params:{id: id}}) 刷新页面的时候会丢失参数，换成this.$router.push({ name: 'NewsDetail', query: { newsUrl: url } })　就不会丢失了。

16.  ********* 同步的含义 ：一次只能执行一个任务，    
               异步就是 ：一次可以执行多个。异步函数也就意味着该函数的执行不会阻塞后面代码的执行。

20. vue数据双向绑定是通过 Object.defineProperty数据劫持结合发布者-订阅者模式的方式来 实现的。

21. ：响应式框架
能让数据与视图非常简单地保持同步。当修改数据的时候，只需要在逻辑层修改，视图层就会做相应的更新。

16. Try语句：定义在执行时进行错误测试的代码块。
    catch 语句：定义当 try 代码块发生错误时，所执行的代码块。
    finally 语句：在 try 和 catch 之后无论有无异常都会执行。

17. vue路由原理 
        通过改变URL，在不重新请求页面的情况下，更新页面视图。

18. null： Null类型，代表“空值”，代表一个空对象指针，使用typeof运算得到 “object”，所以你可以认为它是一个特殊 的 对象值。
undefined： Undefined类型，当一个声明了未赋值，得到的就是undefined。


19.   嵌套路由：父路由中写一个children   代表子路由
        Vue路由如何去#号：可以在路由上加上 mode: 'history',  

21.        hash: 使用变更hash不会刷新页面的特性, 来变更路由, 做到单页面无刷新

6. 在使用计算属性的时，函数名和data数据源中的数据可以同名吗？
  不能同名 因为不管是计算属性还是data还是props 都会被挂载在vm实例上，因此 这三个都不能同名

7. 怎么给vue定义全局的方法
  第一种：挂载到Vue的prototype上。把全局方法写到一个文件里面，然后for循环挂载到Vue的prototype上，缺点是调用这个方法的时候没有提示

第二种：利用全局混入mixin，因为mixin里面的methods会和创建的每个单文件组件合并。这样做的优点是调用这个方法的时候有提示

8. keep-alive有关的什么周期 （长链接）
activated和deactivated两个生命周期函数
当keep-alive组件激活时，触发activated，keep-alive组件停用时调用deactivated

9. template模版的作用 ：当做一个不可见的包裹元素，减少不必要的DOM元素，整个结构会更加清晰。

10. nextTick的原理吗？把微观任务转为宏观任务，具体没了解
（在进行数据获取后，赋值操作芝华士完成了数据模型改变，没有完成视图更新，）

11. 怎么实现换肤 ： 
全局的theme属性然后做class判断或者加载不同的样式文件。一种是编译时换肤 一种是用户操作换肤。编译时换肤可以通过css in js相关技术修改css预处理器的变量 。用户操作换肤 只能内置一些styleb变量供用户选择了

12. 打包慢  
     需要调试 Webpack，该缓存的缓存、不用编译的别编译。具体看项目

13. 盒模型实际宽度的计算：实际宽度=“双margin + 双padding + width + border”
怪异盒子的实际宽度：=双margin + width.
ie6 padding和border会计入宽高

13. FOUC - Flash Of Unstyled Content 文档样式闪烁
    主要原因是样式的 @import 影响，ie浏览器中先去加载 HTML文档的dom元素，后在加载css导致，在<hearer>中加入<link>或者<script>元素就好

14. http请求头里面有什么？
    1，请求类型  2，请求地址 3. 请求参数  4.请求约束

10. cookie保存在浏览器端，session保存在服务器端
a. Cookie是服务器发给客户端的特殊信息，cookie是以文本的方式保存在客户端，每次请求时都带上它
   不设置到期时间，关闭浏览器就清除，设置过期时间关闭不清除。
    cookie只能保存字符串类型
    cookie：单个cookie保存的数据不能超过4kb
    cookie：（1）大小受限

　　　　　　（2）用户可以操作（禁用）cookie，使功能受限

　　　　　　（3）安全性较低

　　　　　　（4）有些状态不可能保存在客户端。

　　　　　　（5）每次访问都要传送cookie给服务器，浪费带宽。

　　　　　　（6）cookie数据有路径（path）的概念，可以限制cookie只属于某个路径下。

    　session：（1）Session保存的东西越多，就越占用服务器内存，对于用户在线人数较多的网站，服务器的内存压力会比较大。

　　　　　　（2）依赖于cookie（sessionID保存在cookie），如果禁用cookie，则要使用URL重写，不安全

　　　　　　　　（3）创建Session变量有很大的随意性，可随时调用，不需要开发者做精确地处理，所以，过度使用session变量将会导致代码不可读而且不好维护。

11. 具体来说，Web Storage又分为两种：

    1.sessionStorage：将数据保存在session对象中。所谓session，是指用户在浏览某个网站时，从进入网站到浏览器关闭所经过的这段时间，也就是用户浏览这个网站所花费的时间。session对象可以用来保存在这段时间内所要求保存的任何数据。

    2.localStorage：将数据保存在客户端本地的硬件设备(通常指硬盘，也可以是其他硬件设备)中，即使浏览器被关闭了，该数据仍然存在，下次打开浏览器访问网站时仍然可以继续使用。
    
    cookie  是浏览器与服务器之间的交互， session/local 是本地存储