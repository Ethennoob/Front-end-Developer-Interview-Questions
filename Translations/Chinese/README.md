前端工作面试问题

本文包含了一些用于考查候选者的前端面试问题。不建议对单个候选者问及每个问题 (那需要好几个小时)。只要从列表里挑选一些，就能帮助你考查候选者是否具备所需要的技能。

备注： 这些问题中很多都是开放性的，可以引发有趣的讨论。这比直接的答案更能体现此人的能力。

目录

1. 常见问题
   1. HTML 相关问题
   2. CSS 相关问题
   3. JS 相关问题
   4. 测试相关问题
   5. 效能相关问题
   6. 网络相关问题
   7. 代码相关问题
   8. 趣味问题

参与协作

1. 贡献者
   1. 如何参与贡献
   2. 许可协议

常见问题：

- 你在昨天/本周学到了什么？
      这段时间一直在整理有关前端的面试题目，整理这也题目，不只是为了能够学习应付即将到来的面试，更是为了补补基础知识。日常项目开发进度太快了，很多属性或者方法用了就忘，这样会造成另外一个隐患，因为基本知识不够扎实，常用的方法用得不够熟练，就很难高效率地开发项目。·　　有了扎实的基础知识，才能其期盼自己走得更远。　　
      
      1）我最近学习了Node.js ,Node.js是一个Javascript运行环境(runtime),Node.js使用Module模块去划分不同的功能，以简化应用的开发,Modules模块有点像C++语言中的类库。每一个Node.js的类库都包含了十分丰富的各类函数，比如http模块就包含了和http功能相关的很多函数，可以帮助开发者很容易地对比如http,tcp/udp等进行操作，还可以很容易的创建http和tcp/udp的服务器。
      
      2）知道了CSS的“层叠”规则，整理并且对比了清楚浮动和实现居中的方法，还发现了一些不常用属性。于是，有利于日后高效地编写样式表。　　
      
      等等，等等(这种问题只有自己清楚)
- 编写代码的哪些方面能够使你兴奋或感兴趣？
      编写代码最让我兴奋的是学习新的技术，尝试新的视觉效果的过程，而且本着程序员这一行也是目前互联网时代最重要的岗位，我热爱这份工作。
      
      前端本身就是一个美好有趣的领域。对于众多的网站或者系统来说，后台提供的功能才是核心模块，但是关乎网站或者系统是否能够持续地吸引用户的眼球，能否在同样类型的产品中脱颖而出，也许前端的交互是否人性化和性能是否稳定高效占了绝大多数因素。良好的用户体验，给他们积极高效的用户体验，甚至改变大众的生活方式，这正是我当初学习编程的初衷。
      
      面试官也许会问得：是怎么实现这个效果的或者关于用户体验方面你还做过哪些努力，没关系，我认真做了准备。甚至要对比一下css3过渡和动画的区别，关于css3的具体使用就不在这里列举，用户体验方面的答案，下面会做回答。
      /*@keyframes 规则用于创建动画。在 @keyframes 中规定某项 CSS 样式，就能创建由当前样式逐渐改为新样式的动画效果。*/
      @-webkit-keyframes spin {
      　　0% {
      　　　　-webkit-transform:rotate(0deg);
      　　}
      　　50% {
      　　　　-webkit-transform:rotate(-180deg);
      　　}
      　　100% {
      　　　　-webkit-transform:rotate(-360deg);
      　　}
      }
      /*使用 @keyframes 中创建动画，需要把它捆绑到某个选择器，否则不会产生动画效果。
      通过规定至少以下两项 CSS3 动画属性，即可将动画绑定到选择器：
      　　　　规定动画的名称
      　　　　规定动画的时长
      */
      -webkit-animation:spin 1.5s linear infinite;
      -moz-animation:spin 1.5s linear infinite;
- 你最近遇到过什么技术挑战？你是如何解决的？
- 在制作一个网页应用或网站的过程中，你是如何考虑其 UI、安全性、高性能、SEO、可维护性以及技术因素的？
      UI：界面美观，要有个性，考虑用户使用的逻辑要简单，用起来舒适自由。使用习惯要符合大部分用户的习惯，比如少让用户输入，采用选择的方式，提供搜索和提示功能。
      
      安全性：
        1、对输入进行有效性验证(例如验证手机号码和email的正则验证)
      
        2、对交互操作进行身份验证和授权(例如给手机号码发送验证码)
      
        3、异常错误处理（向用户反馈单额错误提示不要让攻击者分析出一些网络环境和配置）
      
      高性能：(可以不看)
      1、DNS（域名系统）负载均衡；在DNS中为多个IP地址配置同一个域名如：www.baidu.com，因而查询这个域名的客户机将得到其中一个地址，从而使得不同的客户访问不同的服务器，达到负载均衡的目的，从而减小服务器端的压力。
      
      DNS负载均衡是一种简单而有效的方法，但是它不能区分服务器的差异，也不能反映服务器的当前运行状态。
      
      2、HTTP重定向（通过使客户端重定向，来分散和转移请求压力，比如一些下载服务通常都有几个镜像服务器）；301重定向是网址重定向最为可行的一种办法,seo最为友好。
      3、 分布式缓存；参照http://www.07net01.com/program/374570.html
      4、数据库扩展：读写分离，垂直分区，水平分区
      5、反向代理负载均衡：让代理服务器将请求均匀转发给多台内部Web服务器之一上,从而达到负载均衡的目的。这种代理方式与普通的代理方式有所不同,标准代理方式是客户使用代理访问多个外部Web 服务器,而这种代理方式是多个客户使用它访问内部Web服务器,因此也被称为反向代理模式。
      使用反向代理的好处是,可以将负载均衡和代理服务器的高速缓存技术结合在一起,提供有益的性能,具备额外的安全性,外部客户不能直接访问真实的服务器。并且实现起来可以实现较好的负载均衡策略,将负载可以非常均衡的分给内部服务器,不会出现负载集中到某个服务器的偶然现象。
      
      SEO:选好关键字，描述语言，修饰性图片换成文本，合理使用h1-h6，对图片添加alt属性，链接添加target属性。
      
      可维护性：代码是否容易被理解，是否容易被修改和增加新的功能，当出现问题时是否能快速定位到问题代码。
- 请谈谈你喜欢的开发环境。
      目前我的开发环境都仅限于在Windows上，系统是Windows 10，编辑器是Hbuilder和sublime text，服务器环境是apache2或Node.js。浏览器使用chrome，内部提供的开发工具很丰富。
      不过Unix系统才是程序员的最优系统选择，以后我会选择MacOS上面编程。
- 你最熟悉哪一套版本控制系统？
      git和svn都用过，不过git的使用仅限于可视化工具(利用软件操作)，命令行不熟悉。svn的使用是因为在学校做大作业我选择用tortoiseSVN将代码上传到新浪云服务器，然后给老师演示我的作业。
      
      扩展：
      
      在Git 中的绝大多数操作都只需要访问本地文件和资源，不用连网。对于任何一个文件，在Git 内都只有三种状态：已提交（committed），已修改（modified）和已暂存（staged）。已提交表示该文件已经被安全地保存在本地数据库中了；已修改表示修改了某个文件，但还没有提交保存；已暂存表示把已修改的文件放在下次提交时要保存的清单中。·基本的Git 工作流程如下所示：
      
      1. 在工作目录中修改某些文件。
      2. 对这些修改了的文件作快照，并保存到暂存区域。
      3. 提交更新，将保存在暂存区域的文件快照转储到git 目录中。
      常用命令：
      //用git 把Git 项目仓库克隆到本地，以便日后随时更新：
      $ git clone git://git.kernel.org/pub/scm/git/git.git
      //git add 命令告诉Git 开始对
      这些文件进行跟踪，然后提交：
      $ git add filenme.html
      //每次准备提交前，先用git status 看下，是不是都已暂存起来了，然后再运行提交命令
      $ git commit -m 'initial project version'
      // 把本地仓库提交到远程仓库的master分支中
      $ git push origin master
- 你能描述当你制作一个网页的工作流程吗？
  作为一名现代前端工程师
      1)一同和产品大致过一遍产品需求
      2）一同和UI设计讨论UI的设计问题，特别是一些交互细节，避免在开发过程中过多的打断开发要临时去询问交互细节
      3）确立基本网站框架，例如vuejs，图标使用iconfont。
      4）从版本工具中创建创建项目。
      5）编码开发调试（包括还原页面，绑定数据）。
      6）自己进行测试几遍。
      7）提交上传供测试人员测试。
- 假若你有 5 个不同的样式文件 (stylesheets), 整合进网站的最好方式是?
      文件拼合，减少http请求。
      
      用一个大的CSS文件替代多个小体积的CSS文件这是一个很好的实践，可以获得更好的可维护性，但是在网站性能方面会产生一定的影响（这里指的是随着文件体积的增大，随之消耗服务器的内存也会增加）。尽管你应该把CSS文件拆分成小块，但是当浏览器请求这些文件时，会产生同等数量的http请求。每个http请求都会产生一次从你的浏览器到服务器端网络往返过程，并且导致推迟到达服务器端和返回浏览器端的时间，我们称之为延迟。因此，如果你有4个Javascript和3个css文件在页面中被加载，你浪费掉了7次因网络往返过程产生的时间。浏览器在你的CSS完全加载完成之前是不能很好的渲染你的页面的。因此越多的延迟让你的页面载入越慢。
- 你能描述渐进增强 (progressive enhancement) 和优雅降级 (graceful degradation) 之间的不同吗?
      它们是看待同种事物的两种观点，它们关注在同一个网站同一功能在不同设备不同浏览器下的表现：
      
      渐进增强，一开始值构建站点的最小特性，然后不断针对个浏览器追加功能，性能越好的设备能够显示更加出众的效果。
      
      优雅降级，一开始就构造站点的完整功能，然后针对浏览器测试和修复。
      
      web标准对可访问性做了如下定义：web内容对于残障用户或者普通的可阅读和可理解性。无论用户是否残障，都得通过用户代理（User Agent）来访问Web内容。因此要提高可访问性，首先得考虑各种用户代理 ：桌面浏览器、语音浏览器、移动电话、车载个人电脑等等。还得考虑用户访问Web内容时的环境限制 。比如：我们真的要考虑浏览器禁用JavaScript/CSS的情形吗？我的理解是，要考虑的其实不是禁用了JavaScript/CSS的浏览器，而是那些对JavaScript/CSS不支持或支持不好的用户代理。比如语音阅读器，手机浏览器等，JavaScript提供的是一层可访问性，不能代替内容本身。
      
      当然，从渐进增强的角度讲，鼓励使用高级特性，只是同时要做到优雅降级，让低端用户代理上，也能保留低保真的体验。（除了用户代理，还有什么方法检测客户端设备？特性检测，css3媒体查询）
      
      (讲讲我在平时项目中，在“渐进增强”和“优雅降级”的努力)
      
      如果提到了特性检测，可以加分。
- 你如何对网站的文件和资源进行优化？
      文件合并（同上题“假若你有5个不同的 CSS 文件, 加载进页面的最好方式是？”）
      减少调用其他页面、文件的数量。一般我们为了让页面生动活泼会大量使用background来加载背景图，而每个 background的图像都会产生1次HTTP请求，要改善这个状况，可以采用css的1个有用的background-position属 性来加载背景图，我们将需要频繁加载的多个图片合成为1个单独的图片，需要加载时可以采用：background:url(....) no-repeat x-offset y-offset;的形式加载即可将这部分图片加载的HTTP请求缩减为1个。
      
      文件最小化/文件压缩
      即将需要传输的内容压缩后传输到客户端再解压，这样在网络上传输的 数据量就会大幅减小。通常在服务器上的Apache、Nginx可以直接开启这个设置，也可以从代码角度直接设置传输文件头，增加gzip的设置，也可以 从 负载均衡设备直接设置。不过需要留意的是，这个设置会略微增加服务器的负担。建议服务器性能不是很好的网站，要慎重考虑。
      
      使用 CDN 托管
      CDN的全称是Content Delivery Network，即内容分发网络。其基本思路是尽可能避开互联网上有可能影响数据传输速度和稳定性的瓶颈和环节，使内容传输的更快、更稳定。其目的是使用户可就近取得所需内容，解决 Internet网络拥挤的状况，提高用户访问网站的响应速度。
      
      缓存的使用
      ajax调用都采用缓存调用方式，一般采用附加特征参数方式实现，注意其中的<script src=”xxx.js?{VERHASH}”，{VERHASH}就是特征参数，这个参数不变化就使用缓存文件，如果发生变化则重新下载新文件或更新信息。
      
      css文件放置在head，js放置在文档尾部
      在服务器端配置control-cache  last-modify-date
      在服务器配置Entity-Tag     if-none-match
- 浏览器同一时间可以从一个域名下载多少资源？
  即浏览器并发请求数。同一时间针对同一域名下的请求有一定数量限制。超过限制数目的请求会被阻止。（借用百度上的一张图片）
  
  - 有什么例外吗？
        加分项： 指出在手机端可能有负面影响 
        加分项： HTTP2 / SPDY
- 请说出三种减少页面加载时间的方法。(加载时间指感知的时间或者实际加载时间)
      关于实际加载时间，可以使用上题”你如何对网站的文件和资源进行优化？“方法。
      
      关于感知时间，可以使用上题“编写代码的哪些方面能够使你兴奋或感兴趣？”答案。
- 如果你参与到一个项目中，发现他们使用 Tab 来缩进代码，但是你喜欢空格，你会怎么做？
      为了保持一致性，接受项目原有的风格
- 请写一个简单的幻灯效果页面。
      你自己可以的嘻嘻☺️
- 如果今年你打算熟练掌握一项新技术，那会是什么？
      对于我来讲，目前Node.js是我想熟练掌握的。感觉上身为一名前端居然可以向后端进阶，想成为小全栈😏
- 请谈谈你对网页标准和标准制定机构(W3C)重要性的理解。
      关于W3C标准，要求：
      
      1）书写闭合，标签小写、不乱嵌套。有利于SEO(还记得以前董大力给你指出的ui>li就能完成的列表你还在里面嵌套div😓)
      
      2）尽量使用外链的css和js脚本，结构(html)行为(js)表现(css)分离。有利于页面加载速度加快。
      
      3）样式和标签分离，使用更合理的语义化标签，内容被更多用户设备访问，维护成本也会降低。
- 什么是 FOUC (无样式内容闪烁)？你如何来避免 FOUC？
      某些页面在Windows 下的Internet Explorer(IE浏览器)出现一些奇怪的现象:以无样式显示页面内容的瞬间闪烁,这种现象称之为文档样式短暂失效(Flash of Unstyled Content),简称为FOUC.原因大致为：
      1，使用import方法导入样式表。
      2，将样式表放在页面底部
      3，有几个样式表，放在html结构的不同位置。其实原理很清楚：当样式表晚于 结构性html 加载，当加载到此样式表时，页面将停止之前的渲染。此样式表被下载和解析后，将重新渲染页面，也就出现了短暂 的 花屏现象。
      
      解决方法：使用LINK标签将样式表放在文档HEAD中更多
- 关于页面渲染过程
      1）解析HTML代码，生成一棵DOM树
      
      2）解析CSS文件
      
      3）生成渲染树（受样式影响，包含不可见元素）
      
      4）渲染树中的节点
- 请解释 CSS 动画和 JavaScript 动画的优缺点。
      CSS3的动画的优点：
      　　1.在性能上会稍微好一些，浏览器会对CSS3的动画做一些优化（比如专门新建一个图层用来跑动画）
      　　2.代码相对简单
      　　但其缺点也很明显：
      　　1.在动画控制上不够灵活
      　　2.兼容性不好
      　　3.部分动画功能无法实现（如滚动动画，视差滚动等）
      　　
      JavaScript的动画正好弥补了这两个缺点，控制能力很强，可以单帧的控制、变换，同时写得好完全可以兼容IE6，并且功能强大。但想想CSS动画的transform矩阵是C++级的计算，必然要比javascript级的计算要快。另外对库的依赖也是一个很让人头疼的问题。
      
      　　所以，对于一些复杂控制的动画，使用javascript会比较靠谱。而在实现一些小的交互动效的时候，就多考虑考虑CSS吧。
- 什么是跨域资源共享 (CORS)？它用于解决什么问题？

HTML 相关问题：

- doctype(文档类型) 的作用是什么？
      位于html标签最前面，告诉浏览器以那种html和xhtml规范。分为标准模式和怪异模式、基于框架的HTML模式。假如浏览器不以doctype标准模式编写DTD，页面除了无法通过代码检验之外，还无法在浏览器中正确显示。
- 浏览器标准模式 (standards mode) 和怪异模式 (quirks mode) 之间的区别是什么？
      当浏览器厂商开始创建与标准兼容的浏览器时，他们希望确保向后兼容性。为了实现这一目的，他们创建了两种呈现模式，标准和混杂模式。在标准模式中，浏览器会根据规范呈现页面；在混杂模式中。页面会以一种相对宽松的向后兼容方式显示。混杂模式常用于模拟老式浏览器的行为，以防止老站点无法工作。
      
      他们最大的不同是对盒模型的解析。
      
      如：在标准模式中 ：width是内容宽度 ，也就是说,元素真正的宽度 = margin-left + border-left-width + padding-left + width + padding-right + border-right- width +  margin-right;
      
      在怪异模式中 ：width则是元素的实际宽度 ，内容宽度 = width - (margin-left + margin-right + padding-left + padding-right + border-left-width + 　border-right-width)
      
      使用 document.compatMode来判断浏览器的解析方式。
- HTML 和 XHTML 有什么区别？
      xhtml要求严格：放弃了一些语义不好的标签，必须有head、body，每个dom必须要闭合。一些老的浏览器并不兼容。
- 如果页面使用 'application/xhtml+xml' 会有什么问题吗？
      为contentType属性值，IE不支持application/xhtml+xml类型，支持text/html
- 如果网页内容需要支持多语言，你会怎么做？
      使用统一的UTF-8编码
- 在设计和开发多语言网站时，有哪些问题你必须要考虑？
      1）制图时，应该将图形的图像层与文本层分离，这样在重新绘制该图形时只需对文本进行翻译。
      
      2）设置控件属性应考虑到各种语言版本的文本显示，尽可能为翻译预留足够的空间。同时也应该保持不同语言界面的统一性，避免过多的差异。
      
      3）编码注意代码复用，将多个模块的共用信息存放在共通的文件中便于全局管理。
- 使用 data- 属性的好处是什么？
      data-是HTML5为前端开发者提供自定义的属性，这些属性集可以通过对象的dataset属性获取，不支持该属性的浏览器可以通过 getAttribute方法获取。
- 如果把 HTML5 看作做一个开放平台，那它的构建模块有哪些？
      1）Web Storage API(利用sessionStorage或 localStorage做客户端本地存储)
      (sessionStorage将数据保存在session中，浏览器关闭也就没了；而localStorage则一直将数据保存在客户端本地，除非主动删除数据，否则数据是永远不会过期的；)
       1.保存数据： localStorage.setItem( key, value );      
             sessionStorage.setItem( key, value );
       2.读取数据： localStorage.getItem( key );     
             sessionStorage.getItem( key );  
       3.删除单个数据：localStorage.removeItem( key );     
               sessionStorage.removeItem( key );
       4.删除所有数据：localStorage.clear( );     
               sessionStorage.clear( );
       5.得到某个索引的key：localStorage.key( index );     
                  sessionStorage.key( index );
      //大概知道就行了 不重要
      2）基于位置服务LBS
      3）无插件播放音频视频
      4）调用相机和GPU图像处理单元等硬件设备
      5）拖拽和Form API
- 请描述 cookies、sessionStorage 和 localStorage 的区别。
      共同点：都是保存在浏览器端，且同源的。
      
      区别：
      　　1）cookie数据始终在同源的http请求中携带（即使不需要），即cookie在浏览器和服务器间来回传递。而sessionStorage和localStorage不会自动把数据发给服务器，仅在本地保存。
      
      　　2）cookie数据还有路径（path）的概念，可以限制cookie只属于某个路径下。存储大小限制也不同，cookie数据不能超过4k，同时因为每次http请求都会携带cookie，所以cookie只适合保存很小的数据，如会话标识。
      　　3）sessionStorage和localStorage 虽然也有存储大小的限制，但比cookie大得多，可以达到5M或更大。数据有效期不同，sessionStorage：仅在当前浏览器窗口关闭前有效，自然也就不可能持久保持；localStorage：始终有效，窗口或浏览器关闭也一直保存，因此用作持久数据；cookie只在设置的cookie过期时间之前一直有效，即使窗口或浏览器关闭。
      　　4）作用域不同，sessionStorage不在不同的浏览器窗口中共享，即使是同一个页面；localStorage 在所有同源窗口中都是共享的；cookie也是在所有同源窗口中都是共享的。
      
      Web Storage 支持事件通知机制，可以将数据更新的通知发送给监听者。Web Storage 的 api 接口使用更方便。
      
      Web Storage带来的好处：
      　　1）减少网络流量：一旦数据保存在本地后，就可以避免再向服务器请求数据，因此减少不必要的数据请求，减少数据在浏览器和服务器间不必要地来回传递。
      　　2）快速显示数据：性能好，从本地读数据比通过网络从服务器获得数据快得多，本地数据可以即时获得。再加上网页本身也可以有缓存，因此整个页面和数据都在本地的话，可以立即显示。
      　　3）临时存储：很多时候数据只需要在用户浏览一组页面期间使用，关闭窗口后数据就可以丢弃了，这种情况使用sessionStorage非常方便。
      
- 同步与异步
      同步：脚本会停留并等待服务器发送回复然后再继续。提交请求->等待服务器处理->处理完毕返回，这个期间客户端浏览器不能干任何事。
      
      异步：脚本允许页面继续其进程并处理可能的回复。请求通过事件触发->服务器处理（这是浏览器仍然可以作其他事情）->处理完毕
      
      若要在使用ajax请求后处理发送请求返回的结果，最好使用同步请求。
- 请解释 <script>、<script async> 和 <script defer> 的区别。
      1.<script src="example.js"></script>
        没有defer或async属性，浏览器会立即加载并执行相应的脚本。也就是说在渲染script标签之后的文档之前，不等待后续加载的文档元素，读到就开始加载和执行，此举会阻塞后续文档的加载；
      
      2.<script async src="example.js"></script>
        有了async属性，表示后续文档的加载和渲染与js脚本的加载和执行是并行进行的，即异步执行；
      
      3.<script defer src="example.js"></script>
        有了defer属性，加载后续文档的过程和js脚本的加载(此时仅加载不执行)是并行进行的(异步)，js脚本的执行需要等到文档所有元素解析完成之后，DOMContentLoaded事件触发执行之前。
- 为什么通常推荐将 CSS <link> 放置在 <head></head> 之间，而将 JS <script> 放置在 </body> 之前？你知道有哪些例外吗？
      在文档的<head>元素中包含的文件，意味着文件中代码都被下载，解析完之后，才能开始呈现页面的内容（浏览器在遇到<body>标签时才开始呈现内容）。页面的渲染需要在css文件下载完成后执行。Script放在<head>之间会导致呈现页面是出现明显的延迟，所以放在</body>之前。
- 什么是渐进式渲染 (progressive rendering)？
- 你用过哪些不同的 HTML 模板引擎？

CSS 相关问题：

- CSS 中类 (classes) 和 ID 的区别。
      在样式表定义一个样式的时候，可以定义id也可以定义class。
      
      1、在CSS文件里书写时，ID加前缀"#"；CLASS用"."
      
      2、id一个页面只可以使用一次；class可以多次引用。
      
      3、ID是一个标签，用于区分不同的结构和内容，就象名字，如果一个屋子有2个人同名，就会出现混淆；class是一个样式，可以套在任何结构和内容上，就象一件衣服；
      
      4、从概念上说就是不一样的：id是先找到结构/内容，再给它定义样式；class是先定义好一种样式，再套给多个结构/内容。　　　　
      目前的浏览器还都允许用多个相同ID，一般情况下也能正常显示，不过当你需要用JavaScript通过id来控制div时就会出现错误。
- 请问 "resetting" 和 "normalizing" CSS 之间的区别？你会如何选择，为什么？
      resetting:直接重置所有格式，没有任何前提性质的。
      normalizing：重置部分格式的。
      所以建议在设置的时候使用 normalizing进行重置，避免造成所有数据丢失。resetting 这个需要谨慎使用
      
      专门给yumi补充：
      
      Reset是什么？
      我们可以把它叫做CSS重设，也有人叫做CSS复位、默认CSS、CSS重置等。 CSS重设就是由于各种浏览器解释CSS样式的初始值有所不同，导致设计师 在没有定义某个CSS属性时，不同的浏览器会按照自己的默认值来为没有定 义的样式赋值，所以我们要先定义好一些CSS样式，去“覆盖”浏览器的CSS默认属性， 来让所有浏览器都按照同样的规则解释CSS，这样就能避免发生这种问题。
      
      Normalize是什么？
      Normalize.css 只是一个很小的CSS文件，但它在默认的HTML元素样式上 提供了跨浏览器的高度一致性。相比于传统的CSS reset，Normalize.css 是一种现代的、为HTML5准备的优质替代方案。Normalize.css现在已经被 用于Twitter Bootstrap、HTML5 Boilerplate、GOV.UK、Rdio、CSS Tricks 以及许许多多其他框架、工具和网站上。 
- 请解释浮动 (Floats) 及其工作原理。
      问题成因：在一个容器中，有两个浮动的子元素，会造成显示结果意想不到的问题。在CSS规范中，浮动定位不属于正常的页面流，而是独立定位的。
      
      关于css的定位机制：普通流(就是不理它自然地布局)，浮动，绝对定位（position：fixed是position：absolute的一个子类）。
      浮动的框可以左右移动，直到它的外边缘遇到包含框或者另一个浮动框的边缘，所以才说浮动定位不属于正常的页面流。文档中的普通流就会表现得和浮动框不存在一样，当浮动框高度超出包含框的时候，就会出现包含框不会自动伸缩高度类笔盒浮动元素。所以，只含有浮动元素的父容器在显示时不需要考虑子元素的位置，就造成显示父容器像空容器一样。
- 描述z-index和叠加上下文是如何形成的。
      z-index就是控制元素在页面的中的叠加顺序，z-index值高的元素显示在z-index值低的前面。z-index的使用条件：只对有 position 属性的且值不为static的元素才有效。
- 请描述 BFC(Block Formatting Context) 及其如何工作。
      //了解就好,可以跳过
      BFC（Block Formatting Context）直译为“块级格式化范围”。
      
      是 W3C CSS 2.1 规范中的一个概念，它决定了元素如何对其内容进行定位，以及与其他元素的关系和相互作用。当涉及到可视化布局的时候，Block Formatting Context提供了一个环境，HTML元素在这个环境中按照一定规则进行布局。
      
      一个环境中的元素不会影响到其它环境中的布局。比如浮动元素会形成BFC，浮动元素内部子元素的主要受该浮动元素影响，两个浮动元素之间是互不影响的。这里有点类似一个BFC就是一个独立的行政单位的意思。也可以说BFC就是一个作用范围。可以把它理解成是一个独立的容器，并且这个容器的里box的布局，与这个容器外的毫不相干。
- 列举不同的清除浮动的技巧，并指出它们各自适用的使用场景。
      1）添加额外标签
      在浮动元素末尾添加一个空的标签例如 <div style=”clear:both”></div>。
        优点：通俗易懂，容易掌握
        缺点：可以想象通过此方法，会添加多少无意义的空标签，有违结构与表现的分离，在后期维护中将是噩梦。
        
      2）使用 br标签和其自身的 html属性 <br clear="all" />
        优点：比空标签方式语义稍强，代码量较少
        缺点：同样有违结构与表现的分离，不推荐使用
        
      3)父元素设置 overflow：hidden
        通过设置父元素overflow值设置为hidden；在IE6中还需要触发 hasLayout ，例如 zoom：1。<div    class="warp" id="float3" style="overflow:hidden; *zoom:1;">
        优点：不存在结构和语义化问题，代码量极少
        缺点：内容增多时候容易造成不会自动换行导致内容被隐藏掉，无法显示需要溢出的元素；overflow:hidden     会导致中键失效。
        
      4)父元素设置 overflow：auto 属性。同样IE6需要触发hasLayout，演示和3差不多
        优点：不存在结构和语义化问题，代码量极少
        缺点：多个嵌套后，firefox某些情况会造成内容全选；IE中 mouseover 造成宽度改变时会出现最外层模块   有滚动条等，firefox早期版本会无故产生focus等。
        
      5）使用:after 伪元素
        需要注意的是 :after是伪元素（Pseudo-Element），不是伪类（某些CSS手册里面称之为“伪对象”），很多  清除浮动大全之类的文章都称之为伪类，不过csser要严谨一点，这是一种态度。由于IE6-7不支持:after，使  用 zoom:1触发 hasLayout。
      .clearfix:after {
        content:"."; 
        display:block; 
        height:0; 
        visibility:hidden; 
        clear:both; 
      }
      .clearfix { *zoom:1; }
        优点：结构和语义化完全正确,代码量居中
        缺点：复用方式不当会造成代码量增加
- 请解释 CSS sprites，以及你要如何在页面或网站中实现它。
      //老技术
      CSS sprites其实就通过将多个图片融合到一副图里面，然后通过CSS的技术布局到页面上。这样做的好处是，减少图片数量，将会减少http的请求，提升网站性能。
      
      编写css代码background:url(....) no-repeat x-offset y-offset;同时设定元素固定高度和宽度，overflow:hidden
- 你最喜欢的图片替换方法是什么，你如何选择使用。
  有一种方法
       <h2><span></span>Hello World </h2>
      h2 {
          width: 150px;height: 35px;
          position: relative; 
      } 
      h2 span {
          background: url(hello_world.gif) no-repeat; 
          position: absolute; 
          width: 100%; 
          height: 100%; 
      }
      首先，将 H2 的 position 设为 relative ，这样将使 H2 里面的元素定位以 H2 为参照，然后将 SPAN 元素绝对定位，撑满整个 H2 区域，同时将背景图应用在 SPAN 标签里面；这种方法的原理是将 SPAN 标签覆盖在文字内容上面，一旦 SPAN 里面的背景图无法显示，将显示下层的文字内容，不影响正常使用。但是，此方法也有一个缺陷，就是背景图不能透明，否则将透出下面的文字。
- 你会如何解决特定浏览器的样式问题？
      区别不同浏览器，CSS hack写法：
      
      
      区别IE6与FF：
             background:orange;*background:blue;
      
      
      区别IE6与IE7：
             background:green !important;background:blue;
      
      
      区别IE7与FF：
             background:orange; *background:green;
- 如何为有功能限制的浏览器提供网页？
      尽量避免当js或者css3失效时，页面不可用的动画效果。
      
      部分浏览器不支持html5新标签，因此，可以用js创建相关标签，然后给它们的css赋予相关属性。
      
      因为iphone并没有鼠标指针，所以没有hover事件。那么CSS :hover伪类就没用了。但是iPhone有Touch事件，onTouchStart 类似 onMouseOver，onTouchEnd 类似 onMouseOut。所以我们可以用它来模拟hover。
      使用Javascript：
      var myLinks = document.getElementsByTagName('a');
      for(var i = 0; i < myLinks.length; i++){
      　　 myLinks[i].addEventListener(’touchstart’, function(){
          this.className = “hover”;
          }, false);
      　　 myLinks[i].addEventListener(’touchend’, function(){
           this.className = “”;
          }, false);
      }
  然后用CSS增加hover效果：
      a:hover, a.hover { /* 你的hover效果 */ }
- 有哪些的隐藏内容的方法 (如果同时还要保证屏幕阅读器可用呢)？
      需要隐藏内容的几种可能性：
      
      1）对文本的隐藏
      
      2）隐藏超链接（另类黑链）
      
      3）对统计代码隐藏
      
      4）隐藏超出图片
      
      5）css隐藏滚动条
      
      6）css隐藏div层
      
      具体实现：
      
      1、css隐藏DIV及内容，完全隐藏内容与布局。display:none或者visibility:hidden
      
      （面试官也许会问到：关于display:none和visible:hidden区别）
      
      display:none和visible:hidden都能把网页上某个元素隐藏起来，但两者有区别:
      
      display:none ---不为被隐藏的对象保留其物理空间，即该对象在页面上彻底消失，通俗来说就是看不见也摸不到。
      
      visible:hidden--- 使对象在网页上不可见，但该对象在网页上所占的空间没有改变，通俗来说就是看不见但摸得到。
      
      2、通过对象盒子设置缩进样式（text-indent:-9999px）方法可以隐藏超链接文本内容
      同样道理，可以用来隐藏图片上方文字。此类问题我们常见于LOGO处使用，我们想让图片作为背景，而图片上方放A链接文字内容，但html锚文本功能仍然正常也能鼠标点击使用。图片作为背景而html代码内看不到图片，但文字也存在，却是文字隐藏图片显示出，鼠标也能点击指向。
      
      3、overflow: hidden 隐藏溢出DIV内容或图片
      
      4、css隐藏滚动条
      
      使用overflow-y:hidden;和overflow-x:hidden来隐藏或显示对应横或竖方向的滚动条。
- 你用过栅(zha四声)格系统 (grid system) 吗？如果使用过，你最喜欢哪种？
      使用过，我使用过Bootstrap的栅格,Bootstrap内置了一套响应式、移动设备优先的流式栅格系统，随着屏幕设备或视口（viewport）尺寸的增加，系统会自动分为最多12列。
      它包含了易于使用的预定义classe，还有强大的mixin用于生成更具语义的布局。
- 你用过媒体查询，或针对移动端的布局/CSS 吗？
      当然使用过
      
      设备宽度(device-width)未必是布局宽度(width)，为了让非适应性布局与手机相适应，我们跟关心视图宽度，因此需要一种方式来设定宽度，这样可以使用媒体查询检测。
      
      让视图的宽度和设备宽度一致
      
      <meta element = "viewport"content = "width=device initial-scale = 1" >
      
      每种布局，都应该根据目标设备指定固定宽度设计
      
      @media screen and (max-width:320px){}
      
      为移动设备调整网页图像。在最基本的页面，一个移动优化的网站就是其布局、内容、互动都经过调整，以适应移动环境。最常见的做法是使用css媒体查询的功能为不同大小的屏幕提供不同的风格；为较小的屏幕优化布局，可以通过针对移动设备的模块服务。
      
      不同设备的分离设计->根据监视屏幕大小进行设计->（媒体查询，灵活排版，图像结合）
- 你熟悉 SVG 样式的书写吗？
      不熟悉
      //我感觉已经没什么必要学SVG
- 如何优化网页的打印样式？
      //感觉不是很重要
      http://www.jb51.net/web/70358.html
- 在书写高效 CSS 时会有哪些问题需要考虑？
- 使用 CSS 预处理器的优缺点有哪些？
      1）reset。参照上题“描述下 “reset” CSS 文件的作用和使用它的好处”的答案。
      
      2）规范命名。尤其对于没有语义化的html标签，例如div，所赋予的class值要特别注意。
      
      2）抽取可重用的部件，注意层叠样式表的“优先级”。
  - 请描述你曾经使用过的 CSS 预处理器(sass)的优缺点。
        提供了许多便利的写法，大大节省了设计者的时间，使得CSS的开发，变得简单和可维护
        缺点我暂时想不出,感觉没有缺点😂
- 如果设计中使用了非标准的字体，你该如何去实现？
      跟产品沟通，尽量使用默认就有的字体
      
      图片替代(一些奇葩的艺术字)
- 请解释浏览器是如何判断元素是否匹配某个 CSS 选择器？
- 请描述伪元素 (pseudo-elements) 及其用途。
- 请解释你对盒模型的理解，以及如何在 CSS 中告诉浏览器使用不同的盒模型来渲染你的布局。
      网页设计中常听的属性名：内容(content)、填充(padding)、边框(border)、边界(margin)，CSS盒子模式都具备这些属性。
      
      每个盒子都有：边界、边框、填充、内容四个属性；
      
      每个属性都包括四个部分：上、右、下、左；这四部分可同时设置，也可分别设置；
- 请解释 * { box-sizing: border-box; } 的作用, 并且说明使用它有什么好处？
      使用 * { box-sizing: border-box; }能够统一IE和非IE浏览器之间的差异。
- 请罗列出你所知道的 display 属性的全部值
      display 属性规定元素应该生成的框的类型。
  
- 请解释 inline 和 inline-block 的区别？
      display:block
      
      1）block元素会独占一行，多个block元素会各自新起一行。默认情况下，block元素宽度自动填满其父元素宽度。
      
      2）block元素可以设置width,height属性。块级元素即使设置了宽度,仍然是独占一行。
      
      3）block元素可以设置margin和padding属性。
      
      display:inline
      
      1）inline元素不会独占一行，多个相邻的行内元素会排列在同一行里，直到一行排列不下，才会新换一行，其宽度随元素的内容而变化。
      
      2）inline元素设置width,height属性无效。
      
      3）inline元素的margin和padding属性，水平方向的padding-left, padding-right, margin-left, margin-right都产生边距效果；但竖直方向的padding-top, padding-bottom, margin-top, margin-bottom不会产生边距效果。
      
      display:inline-block
      
      简单来说就是将对象呈现为inline对象，但是对象的内容作为block对象呈现。之后的内联对象会被排列在同一行内。比如我们可以给一个link（a元素）inline-block属性值，使其既具有block的宽度高度特性又具有inline的同行特性。
- 请解释 relative、fixed、absolute 和 static 元素的区别
      在用CSS+DIV进行布局的时候，一直对position的四个属性值relative,absolute,static,fixed分的不是很清楚，以致经常会出现让人很郁闷的结果。今天研究了一下，总算有所了解。在此总结一下：
      
      先看下各个属性值的定义：
      
      1、static：默认值。没有定位，元素出现在正常的流中（忽略 top, bottom, left, right 或者 z-index 声明）。
      
      2、relative：生成相对定位的元素，通过top,bottom,left,right的设置相对于其正常位置进行定位。可通过z-index进行层次分级。
      
      3、absolute：生成绝对定位的元素，相对于 static 定位以外的第一个父元素进行定位。元素的位置通过 "left", "top", "right" 以及 "bottom" 属性进行规定。可通过z-index进行层次分级。
      
      4、fixed：生成绝对定位的元素，相对于浏览器窗口进行定位。元素的位置通过 "left", "top", "right" 以及 "bottom" 属性进行规定。可通过z-index进行层次分级。
- CSS 中字母 'C' 的意思是叠层 (Cascading)。请问在确定样式的过程中优先级是如何决定的 (请举例)？如何有效使用此系统？
- 你在开发或生产环境中使用过哪些 CSS 框架？你觉得应该如何改善他们？
      Bootstrap是基于HTML5和CSS3开发的，它在jQuery的基础上进行了更为个性化和人性化的完善，形成一套自己独有的网站风格，并兼容大部分jQuery插件。
      
      Bootstrap中包含了丰富的Web组件，根据这些组件，可以快速的搭建一个漂亮、功能完备的网站。
- 请问你有尝试过 CSS Flexbox 或者 Grid 标准规格吗？
      没有
- 为什么响应式设计 (responsive design) 和自适应设计 (adaptive design) 不同？
      自适应布局（Adaptive Layout）
      
      自适应布局（Adaptive）的特点是分别为不同的屏幕分辨率定义布局。布局切换时页面元素发生改变，但在每个布局中，页面元素不随窗口大小的调整发生变化。就是说你看到的页面，里面元素的位置会变化而大小不会变化；你可以把自适应布局看作是静态布局的一个系列。
      
      流式布局（Liquid Layout）
      
      流式布局（Liquid）的特点（也叫"Fluid") 是页面元素的宽度按照屏幕进行适配调整，主要的问题是如果屏幕尺度跨度太大，那么在相对其原始设计而言过小或过大的屏幕上不能正常显示。
      
      响应式布局（Responsive Layout）
      
      分别为不同的屏幕分辨率定义布局，同时，在每个布局中，应用流式布局的理念，即页面元素宽度随着窗口调整而自动适配。
      
      可以把响应式布局看作是流式布局和自适应布局设计理念的融合。
- 你有兼容 retina 屏幕的经历吗？如果有，在什么地方使用了何种技术？
      科普一下，retina 屏幕就是苹果笔记本使用的屏幕，显示图片和色彩的时候和我们一般显示器不一样
- 请问为何要使用 translate() 而非 absolute positioning，或反之的理由？为什么？

JS 相关问题：

- 请解释事件代理 (event delegation)。
      事件代理在JS世界中一个非常有用也很有趣的功能。当我们需要对很多元素添加事件的时候，可以通过将事件添加到它们的父节点而将事件委托给父节点来触发处理函数。这主要得益于浏览器的事件冒泡机制
      
      事件代理也称为事件委托，利用了事件冒泡。例如：
      <ul class="item-list">
          <li class="item">item1</li>
          <li class="item">item2</li>
          <li class="item">item3</li>
      </ul>
  当页面li增多时单独给每个li元素添加事件处理程序既繁琐又容易出错，利用事件冒泡，在ul去监听事件，li产生事件往上冒泡时去捕获，利用e.target来判断是否为我们的目标元素，是的话就可以做相应操作了。
- 请解释 JavaScript 中 this 是如何工作的。
  - 作为独立函数的调用
      function func(){
          console.log(this);
      }
      
      
      func();
      //Window
  全局作用域中声明一个函数,并调用它,此时函数中的this指向全局对象。
  - 作为对象方法调用
      function say(){
          console.log(this);
      }
      
      var obj = {
          name: "f2er",
          say: say
      };
      
      obj.say();
      //Object {name: "f2er"}
  当函数作为一个对象的方法调用时,函数中的this绑定到了这个对象。
  - 使用call或apply来调用函数
      function func(){
          console.log(this);
      }
      
      var obj = {
          name:"f2er"
      };
      
      func.call(obj);
      //Object {name: "f2er"}
      
      func.apply(obj);
      //Object {name: "f2er"}
  当使用call()或apply()函数进行函数调用时,传入参数对象的将被设置为函数体内this的值,这两个函数都是设置调用函数体内的this值的,且第一个参数都为this,区别是第二个参数apply()是一个参数arguments(类数组对象),而call(),传递给他的是一系列参数。
  - new来调用函数
      function F2er(name){
          this.name = name;   
          console.log(this);
      }
      
      var f2er = new F2er('f2er');
      // F2er {name: "f2er"}
  当使用new来调用一个函数时,会创建一个新的对象,然后绑定到Dog()调用中的this。
- 请解释原型继承 (prototypal inheritance) 的原理。
  先上一个例子:
      function Super(){
          this.superValue = "super";
      }
      
      Super.prototype.getSuperValue = function (){
          return this.superValue;
      }
      
      function Sub(){
          this.subValue = "sub";
      }
      
      var superInstance = new Super();
      
      Sub.prototype = superInstance;
      
      Sub.prototype.getSubValue = function (){
          return this.subValue;
      }
      
      var instance = new Sub();
      console.log(instance.getSuperValue());
      // super
  每个函数Sub都有一个属性prototype，prototype指向一个原型对象，原型对象中也有一个指向函数的属性constructor，通过new一个函数Sub可以产生实例instance，调用这个instance的某个属性或方法时，instance会先查找自身是否有这个方法或者属性，没有的话就会去实例的构造函数Sub的原型prototype中查找，即Sub.prototype，如果给原型对象Sub.prototype赋予另一个类型的实例superInstance，则是在superInstance中查找的，这个superInstance中也有属性prototype指向某个原型对象，以此一级级往上最终到Object.prototype，这样就形成了原型继承。
  利用此原理可以自己实现一个inherits函数：
      function inherits(subType, superType){
          var _prototype = Object.create(superType.prototype);
          _prototype.constructor = subType;
          subType.prototype = _prototype;
      }
- 你怎么看 AMD vs. CommonJS？
      这个我不懂
- 请解释为什么接下来这段代码不是 IIFE (立即调用的函数表达式)：function foo(){ }();.
      (function fn(){..})(),函数被包含在一个括号内,变成为一个表达式,随后跟着一个(),就立即执行这个函数,
      
      这种模式就是立即执行函数表达式(Immediately Invoked Function Expression),简称IIFE。
      
      ﻿也有用(function fn(){..}())后面的括号在前面的括号内这种形式表示的,这两种形式在功能上都是一致的。
      
      IIFE的一些作用:
      
      创建作用域,内部保存一些大量临时变量的代码防止命名冲突。
      一些库的外层用这种形式包起来防止作用域污染。
      运行一些只执行一次的代码。
  - 要做哪些改动使它变成 IIFE?
- 描述以下变量的区别：null，undefined 或 undeclared？
  - 该如何检测它们？
- 什么是闭包 (closure)，如何使用它，为什么要使用它？
  当某个函数调用时会创建一个执行环境以及作用域链，然后根据arguments和其它命名参数初始化形成活动对象。在外部函数调用结束后，其执行环境与作用域链被销毁，但是其活动对象保存在了闭包之中，最后在闭包函数调用结束后才销毁。简单的说，闭包就是能够读取其他函数内部变量的函数。在js中，闭包是指有权访问另一个函数作用域中的变量的函数。
  闭包的作用
  - 匿名自执行函数
  有的场景下函数只需要执行一次，例如init()之类的函数，其内部变量无需维护，我们可以使用闭包。 我们创建了一个匿名的函数，并立即执行它，由于外部无法引用它内部的变量，因此在函数执行完后会立刻释放资源，而且不污染全局对象。
  - 封装
  模拟面向对象的代码风格进行封装，使私有属性存在成为可能。
  缺点
  - 常驻内存，会增大内存使用量，易造成内存泄露
- 请举出一个匿名函数的典型用例？
      $.("input").each(function(e){
        this.val('OK')
      });
- 你是如何组织自己的代码？是使用模块模式，还是使用经典继承的方法？
- 请指出 JavaScript 宿主对象 (host objects) 和原生对象 (native objects) 的区别？
      宿主对象是指DOM和BOM。
      原生对象是Object、Function、Array、String、Boolean、Number、Date、RegExp、Error、Math等对象。
- 请指出以下代码的区别：function Person(){}、var person = Person()、var person = new Person()？
      function Person(){}
      声明一个函数Person()。
      
      var person = Person()
      将函数Person()的结果返回给变量person，如果没有返回值则person为undefined。
      
      var person = new Person()
      new一个Person的实例对象。

- .call 和 .apply 的区别是什么？
  .call和.apply的共同点是都是用来改变函数体内this对象的值。
  区别是第二个参数不一样。apply()的第二个参数是一个类数组对象arguments,参数都是以数组的形式传入,而call(),传递给他的是一系列参数。例如
      Math.max.call(null, 1, 2, 3, 4);
      //4
      
      Math.max.apply(null, [1, 2, 3, 4]);
      //4
- 请解释 Function.prototype.bind？
  Function.prototype.bind方法会创建一个新函数，当这个新函数被调用时，它的this值是传递给bind()的第一个参数, 它的参数是bind()的其他参数和其原本的参数.
  Function.prototype.bind的实现类似于:
      Function.prototype.bind = function (scope) {
          var fn = this;
          return function () {
              return fn.apply(scope, arguments);
          };
      }
  Function.prototype.bind的作用
  - 创建绑定函数
  - 一些函数的参数常常也是函数，给当做参数的函数绑定this值确保参数函数执行时有正确的this指向。
- 在什么时候你会使用 document.write()？
       1.页面载入过程中，用脚本加入新的页面内容。
       2.用延时脚本创建本窗口或新窗口的内容。
- 请指出浏览器特性检测，特性推断和浏览器 UA 字符串嗅探的区别？
- 请尽可能详尽的解释 Ajax 的工作原理(很重要,调后台接口就靠它)。
  Ajax是无需刷新页面就能从服务器取得数据的一种方法。
  原理
  Ajax通过XmlHttpRequest对象来向服务器发异步请求，从服务器获得数据，然后用javascript来操作DOM更新页面。
  过程
  1. 创建XMLHttpRequest对象。
  2. 设置响应HTTP请求的回调函数。
  3. 创建一个HTTP请求，指定相应的请求方法、url等。
  4. 发送HTTP请求。
  5. 获取服务器端返回的数据。
  6. 使用JavaScript操作DOM更新页面。
  缺点
  - 对搜索引擎不友好
  - 要实现Ajax下的前后退功能成本较大
  - 跨域问题限制
- 使用 Ajax 都有哪些优劣？
      (1).AJAX的优点
      
      <1>.无刷新更新数据。
      
      AJAX最大优点就是能在不刷新整个页面的前提下与服务器通信维护数据。这使得Web应用程序更为迅捷地响应用户交互，并避免了在网络上发送那些没有改变的信息，减少用户等待时间，带来非常好的用户体验。
      
      <2>.异步与服务器通信。
      
      AJAX使用异步方式与服务器通信，不需要打断用户的操作，具有更加迅速的响应能力。优化了Browser和Server之间的沟通，减少不必要的数据传输、时间及降低网络上数据流量。
      
      <3>.前端和后端负载平衡。
      
      AJAX可以把以前一些服务器负担的工作转嫁到客户端，利用客户端闲置的能力来处理，减轻服务器和带宽的负担，节约空间和宽带租用成本。并且减轻服务器的负担，AJAX的原则是“按需取数据”，可以最大程度的减少冗余请求和响应对服务器造成的负担，提升站点性能。
      
      <4>.基于标准被广泛支持。
      
      AJAX基于标准化的并被广泛支持的技术，不需要下载浏览器插件或者小程序，但需要客户允许JavaScript在浏览器上执行。随着Ajax的成熟，一些简化Ajax使用方法的程序库也相继问世。同样，也出现了另一种辅助程序设计的技术，为那些不支持JavaScript的用户提供替代功能。
      
      <5>.界面与应用分离。
      
      Ajax使WEB中的界面与应用分离（也可以说是数据与呈现分离），有利于分工合作、减少非技术人员对页面的修改造成的WEB应用程序错误、提高效率、也更加适用于现在的发布系统。
      
      (2).AJAX的缺点
      
      <1>.AJAX干掉了Back和History功能，即对浏览器机制的破坏。
- 请解释 JSONP 的工作原理，以及它为什么不是真正的 Ajax。
      注意不是JSON，不是一种东西，我觉得这个不算重点。
- 你使用过 JavaScript 模板系统吗？
      使用过
  - 如有使用过，请谈谈你都使用过哪些库？
        mustache.js
        
        <p>{{name}}</p>
        
        //这个就是mustache.js，你肯定用过的😏
- 请解释变量声明提升 (hoisting)。
  变量的声明前置就是把变量的声明提升到当前作用域的最前面。
  函数的声明前置就是把整个函数提升到当前作用域的最前面(位于前置的变量声明后面)。
      //变量的声明前置
      
      console.log(num);//undefined
      
      var num = 1;
      
      等价于
      
      //变量的声明前置
      
      var num;
      
      console.log(num);//undefined
      
      num = 1;
      
      //函数的声明前置
      
      var num = 1;
      
      console.log(doubleNum(num));//2
      
      function doubleNum(num){
      
          return num*2;
      
      }
      
      等价于
      
      //函数的声明前置
      
      var num;
      
      function doubleNum(num){
      
          return num*2;
      
      }
      
      num = 1;
      
      console.log(doubleNum(num));//2
- 请描述事件冒泡机制 (event bubbling)。
      事件冒泡(event bubbling)，事件最开始时由触发的那个元素身上发生，然后沿着DOM树向上传播，直到document对象。如果想阻止事件起泡，可以使用e.stopPropagation()。
- "attribute" 和 "property" 的区别是什么？
  attribute是一个特性节点，每个DOM元素都有一个对应的attributes属性来存放所有的attribute节点，attributes是一个类数组的容器，说得准确点就是NameNodeMap，总之就是一个类似数组但又和数组不太一样的容器。attributes的每个数字索引以名值对(name=”value”)的形式存放了一个attribute节点。
      <div class="box" id="box" gameid="880">hello</div>
  可以这样来访问attribute节点：
      var elem = document.getElementById( 'box' );
      console.log( elem.attributes[0].name ); // class
      console.log( elem.attributes[0].value ); // box
  property就是一个属性，如果把DOM元素看成是一个普通的Object对象，那么property就是一个以名值对(name=”value”)的形式存放在Object中的属性。要添加和删除property也简单多了，和普通的对象没啥分别：
- 为什么扩展 JavaScript 内置对象不是好的做法？
- 请指出 document load 和 document DOMContentLoaded 两个事件的区别。
- == 和 === 有什么不同？
      ”==”与”===”是不同的,一个是判断值是否相等,一个是判断值及类型是否完全相等。
- 请解释 JavaScript 的同源策略 (same-origin policy)。
- 如何实现下列代码：

    [1,2,3,4,5].duplicator(); // [1,2,3,4,5,1,2,3,4,5]

- 什么是三元表达式 (Ternary expression)？“三元 (Ternary)” 表示什么意思？
      条件表达式？表达式1：表达式2。
      console.log( (a>b)?a:b );
      如果a大于b，输出a，否则输出b
- 什么是 "use strict"; ? 使用它的好处和坏处分别是什么？
      在所有语句之前放一个特定语句"use strict"，就会为整个script标签开启严格模式。
      优点
      消除Javascript语法的一些不严谨之处，减少一些怪异行为;
      消除代码运行的一些不安全之处，保证代码运行的安全；
      提高编译器效率，增加运行速度；
      为未来新版本的Javascript做好铺垫。
      缺点
      严格模式改变了语义。依赖这些改变可能会导致没有实现严格模式的浏览器中出现问题或者错误。
- (不难哦，很容易看懂😯)请实现一个遍历至 100 的 for loop 循环，在能被 3 整除时输出 "fizz"，在能被 5 整除时输出 "buzz"，在能同时被 3 和 5 整除时输出 "fizzbuzz"。
      //请实现一个遍历至 100 的 for loop 循环，
      //在能被 3 整除时输出 "fizz"，在能被 5 整除时输出 "buzz"，
      //在能同时被 3 和 5 整除时输出 "fizzbuzz"。
      for (var i = 1; i <= 100; i++) {
      
          if (i % 3 === 0) {
              if (i % 5 === 0) {
                  alert('fizzbuzz' + i);
                  continue;
              }
              alert('fizz' + i);
              continue;
          } else if (i % 5 === 0) {
              if (i % 3 === 0) {
                  alert('fizzbuzz' + i);
                  continue;
              }
              alert('buzz' + i);
              continue;
          }
      }
- 为何通常会认为保留网站现有的全局作用域 (global scope) 不去改变它，是较好的选择？
      它的意思是: 尽量少在全局作用域定义变量。
      
      目的:
      
      减少名称冲突
      利于模块化
- 为何你会使用 load 之类的事件 (event)？此事件有缺点吗？你是否知道其他替代品，以及为何使用它们？
- 请解释什么是单页应用 (single page app), 以及如何使其对搜索引擎友好 (SEO-friendly)。
      单页应用是指在浏览器中运行的应用，它们在使用期间不会重新加载页面
      
      seo搜索引擎友好
      1.合理的运用网站标签可以让搜索引擎更好的理解网站的层次内容，比如h标签，strong标签等
      2.CSS和JS的优化，尽可能的使用外部导入，从而让网页代码更加简洁，能用CSS就尽量不用JS，毕竟JS对于搜索引擎而言并不友好。
- 使用 Promises 而非回调 (callbacks) 优缺点是什么？
- 使用一种可以编译成 JavaScript 的语言来写 JavaScript 代码有哪些优缺点？
      优点：
      规避一些js 的缺陷
      缺点：
      调试，输出，错定位，麻烦(因为要编译，每次都要编译就很麻烦)
- 你使用哪些工具和技术来调试 JavaScript 代码？
      chrome的F12的开发者工具就很完美了，调试，打断点等等都很方便
- 你会使用怎样的语言结构来遍历对象属性 (object properties) 和数组内容？
- 请解释可变 (mutable) 和不变 (immutable) 对象的区别。
  - 请举出 JavaScript 中一个不变性对象 (immutable object) 的例子？
  - 不变性 (immutability) 有哪些优缺点？
  - 如何用你自己的代码来实现不变性 (immutability)？
- 请解释同步 (synchronous) 和异步 (asynchronous) 函数的区别。
      同步调用，在发起一个函数或方法调用时，没有得到结果之前，该调用就不返回，直到返回结果；
      
      异步调用的概念和同步相对，在一个异步调用发起后，被调用者立即返回给调用者，但调用者不能立刻得到结果，被调用者在实际处理这个调用的请求完成后，通过状态、通知或回调等方式来通知调用者请求处理的结果。
      
      简单地说，同步就是发出一个请求后什么事都不做，一直等待请求返回后才会继续做事；异步就是发出请求后继续去做其他事，这个请求处理完成后会通知你，这时候就可以处理这个回应了。
- 什么是事件循环 (event loop)？
  - 请问调用栈 (call stack) 和任务队列 (task queue) 的区别是什么？
- 解释 function foo() {} 与 var foo = function() {} 用法的区别
      //函数表达式
      var foo = function () {}
      这种方式是声明了个变量，而这个变量是个方法，变量在js中是可以改变的。
      
      //函数声明
      function foo() {}
      这种方式是声明了个方法，foo这个名字无法改变

测试相关问题：

- 对代码进行测试的有什么优缺点？
- 你会用什么工具测试你的代码功能？
- 单元测试与功能/集成测试的区别是什么？
- 代码风格 linting 工具的作用是什么？

效能相关问题：

- 你会用什么工具来查找代码中的性能问题？
- 你会用什么方式来增强网站的页面滚动效能？
- 请解释 layout、painting 和 compositing 的区别。

网络相关问题：

- 为什么传统上利用多个域名来提供网站资源会更有效？
- 请尽可能完整得描述从输入 URL 到整个网页加载完毕及显示在屏幕上的整个流程。
- Long-Polling、Websockets 和 Server-Sent Event 之间有什么区别？
- 请描述以下 request 和 response headers：
  - Diff. between Expires, Date, Age and If-Modified-...
  - Do Not Track
  - Cache-Control
  - Transfer-Encoding
  - ETag
  - X-Frame-Options
- 什么是 HTTP method？请罗列出你所知道的所有 HTTP method，并给出解释。

代码相关的问题：

问题：foo的值是什么？

    var foo = 10 + '20';
    //1020

问题：如何实现以下函数？*

    add(2, 5); // 7
    add(2)(5); // 7
    
    //答案
    var add = function(x,r) {
        if(arguments.length == 1){
           return function(y) { return x + y; };
        }else{
           return x+r;
        }
    };
    console.log(add(2)(5));
    console.log(add(2,5));

问题：下面的语句的返回值是什么？

    "i'm a lasagna hog".split("").reverse().join("");
    
    //答案,记住这个写法，就是调转字符串
    "goh angasal a m'i"

问题：window.foo的值是什么？

    ( window.foo || ( window.foo = "bar" ) );
    
    //答案,考察window是全局变量,考察 || 运算符,
    //可以理解为,先声明了全局foo,然后进行了赋值.
    "bar"

问题：下面两个 alert 的结果是什么？

    var foo = "Hello";
    (function() {
      var bar = " World";
      alert(foo + bar);
    })();
    alert(foo + bar);
    
    'Hello World'//alert弹出
    ReferenceError: bar is not defined(…)//控制台报错

问题：foo.length的值是什么？

    var foo = [];
    foo.push(1);
    foo.push(2);
    
    //2

问题：foo.x的值是什么？

    var foo = {n: 1};
    var bar = foo;
    foo.x = foo = {n: 2};
    
    //Object{n:2}

问题：下面代码的输出是什么？

    console.log('one');
    setTimeout(function() {
      console.log('two');
    }, 0);
    console.log('three');
    
    //'one' 'three' 'two' 延时加载

趣味问题：

- 你最近写过什么的很酷的项目吗？
- 在你使用的开发工具中，最喜欢哪些方面？
- 谁使你踏足了前端开发领域？
- 你有什么业余项目吗？是哪种类型的？
- 你最爱的 IE 特性是什么？
- 你对咖啡有没有什么喜好？

贡献者：

本文档始于 2009 年，是以下作者的合作成果：@paul_irish @bentruyman @cowboy @ajpiano @SlexAxton @boazsender @miketaylr @vladikoff @gf3 @jon_neal @sambreed 和 @iansym。

时至今日，文档已经融入超过 100 位开发者的贡献。
