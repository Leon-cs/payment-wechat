---                 
layout:     post                 
title:       "20170515专题：支付会员"                     
date:       2017-05-15 19:00:00                   
author:     "PaymentGroup"                   
header-img: "img/post-bg-wechat.jpg"                   
---                 
      
## 专题分享      
很荣幸给大家做这次的分享。我先自我介绍一下，我叫龚正，目前在滴滴金融工作。也是刚来不久，之前在美团和美丽说做支付相关的工作。所以今天 给大家介绍一下支付业务中支付会员相关的内容。   
![20170515_193139](http://wechat.lixf.cn/img/20170515_193139.png)   
![20170515_193154](http://wechat.lixf.cn/img/20170515_193154.png)   
我们都知道，支付体系中 如何识别一个用户 是有多种策略的。第三方支付也好 电商也好。但是 这个维度的不同 所建立的会员体系也是不同的。一般看来 第三方中的支付会员体系独立于 电商等业务，所以 我们下面对三个方面进行讲解：   
![20170515_193423](http://wechat.lixf.cn/img/20170515_193423.png)   
![20170515_193441](http://wechat.lixf.cn/img/20170515_193441.png)   
![20170515_193452](http://wechat.lixf.cn/img/20170515_193452.png)   
业务系统在接入支付系统后，一般来说是需要做一个支付账户转换。会员系统中的会员 代表着这个用户在支付系统中的唯一身份。而以这个身份来产生的所有信息，都是这个会员的资产。一般来讲 一个或多个用户 对应一个支付会员。   
![20170515_193635](http://wechat.lixf.cn/img/20170515_193635.png)   
而会员信息 分为两种：(ppt上不够细化)第一种是 资产;第二种是 信息。   
资产 一般包含用户的身份信息 昵称 会员密码等 也包含用户的手机号等。   
信息一般认为是会员的状态 如激活 冻结以及他产生的一些动作等信息。   
好了 我们对支付会员所拥有的信息有了了解 我们再深入一下 细节：   
![20170515_193924](http://wechat.lixf.cn/img/20170515_193924.png)   
支付密码我们都非常的了解，每天都在用。所以我们来聊聊支付密码。   
![20170515_194018](http://wechat.lixf.cn/img/20170515_194018.png)   
图上是我们最常用的支付宝和微信的支付密码输入图。当然还有线下的ATM啦，等等，都在使用6位支付密码。所以 大家都会有疑问，为什么我们的支付密码都是六位呢？   
![20170515_194137](http://wechat.lixf.cn/img/20170515_194137.png)   
PPT中分了三点：防止暴力破解、增加用户体验、方便记忆。之前的支付宝以及银行都尝试过不同位数的支付密码，但是由于长度过长的不方便 ，效率低下，长度过短的，太容易破解   
都使用了6位支付密码。   
![20170515_194343](http://wechat.lixf.cn/img/20170515_194343.png)   
一般来说，支付密码验证的过程是这样的：前端通过加密密码，传递到后端解密，然后使用hash算法算取hash值与后端保存的密码hash进行比较，最后返回成功还是失败。而在密码传输、密码hash中，都是用了安全级别比较高的算法。PPT中简述了一般加密使用的算法。而密码的保存，一般也是使用随机盐的方式，保证会员密码的安全性。   
![20170515_194650](http://wechat.lixf.cn/img/20170515_194650.png)   
我们现在使用iphone非常的多 所以指纹支付也是非常的普及。很多android手机也大部分普及了指纹支付，这对我们的用户体验有了更大的提升。   
![20170515_194749](http://wechat.lixf.cn/img/20170515_194749.png)   
指纹支付流程很简单。通过硬件判断是否成功，优势和劣势大家一想便知。所以，在风控方面考虑。指纹密码验证的安全性要低于6位支付密码的验证。   
![20170515_194900](http://wechat.lixf.cn/img/20170515_194900.png)   
手势密码我们也很常用。   
![20170515_194926](http://wechat.lixf.cn/img/20170515_194926.png)   
![20170515_194939](http://wechat.lixf.cn/img/20170515_194939.png)   
还有一种是免密支付。虽然不需要输入密码 但是依然是通过用户的行为“指纹”来进行判断。   
![20170515_195038](http://wechat.lixf.cn/img/20170515_195038.png)   
实名体系对于支付系统，乃至第三方来讲都是非常重要的。   
![20170515_195120](http://wechat.lixf.cn/img/20170515_195120.png)   
![20170515_195138](http://wechat.lixf.cn/img/20170515_195138.png)   
为了保证资金安全，实名对于第三方公司来说，是至关重要的。包括监管要求、用户安全、以及深度业务的拓展。   
![20170515_195233](http://wechat.lixf.cn/img/20170515_195233.png)   
第三方支付中，实名账户分成三类，每种类型都有不同的限额。   
![20170515_195323](http://wechat.lixf.cn/img/20170515_195323.png)   
![20170515_195335](http://wechat.lixf.cn/img/20170515_195335.png)   
一般支付公司实名主要通过银行卡、通过银行通道对用户进行实名。但是我们发现，越来越多的第三方需要我们传递身份证信息，这也是为了增加三类实名的比例。   
当然啦，通过其他证件如港澳通行证等，以及 查询公积金、缴纳电费等，都可以实名。   
![20170515_195534](http://wechat.lixf.cn/img/20170515_195534.png)   
这个是提供实名查询功能的公司。价格和实名级别都有所不同。   
![20170515_195619](http://wechat.lixf.cn/img/20170515_195619.png)   
如下案例：   
![20170515_195634](http://wechat.lixf.cn/img/20170515_195634.png)   
![20170515_195654](http://wechat.lixf.cn/img/20170515_195654.png)   
![20170515_195705](http://wechat.lixf.cn/img/20170515_195705.png)   
虽然本次分享没有完全把支付系统中的支付会员相关的知识完完全全的讲述给大家，但是从本次分享中 我们也知道了会员系统在支付系统中是至关重要的。   
对于我们支付系统的发展 以及配合监管 是不可或缺的一部分。   
![20170515_195848](http://wechat.lixf.cn/img/20170515_195848.png)   
本次的分享就讲完啦，谢谢大家。[文中涉及的PPT下载地址](http://wechat.lixf.cn/img/hydra支付业务系统-会员系统.pdf)   
   
      
## Q&A      
      
Q：户账分离 是怎么做的，电商会员和支付账户的分离？    
A：根据对支付系统的设计，是通过映射的方式进行分类 电商会员属于业务，而支付账户在支付账户里面，根据需求来定。   
   
Q：一个或多个用户 对应一个支付会员，有例子吗 ？   
A：有些公司是通过自然人来做的。   
   
Q：比如风控系统识别出近期行为接近危险的会员，预先在登录时就要求验证 ，有这种流程没？    
A：是有的   
   
Q：会员中的会员，和支付会员的具体区别场景，能不能再列举下？   
A：会员中的会员是业务，可能分了很多类，很多号，但是支付时，对应的号可能会不同，因为支付代表的是资金，二会员是业务。   
   
Q：会员的黑白灰名单机制是在支付会员系统中么    
A：这个在风控和会员体系中都有   
   
Q：如果冻结了会员，还会影响正常业务不？交易的资金会走到其他户里还是怎么处理，可以讲下这些么？    
A：冻结也分级别,最高的级别是不允许做任何资金操作的,比如监管下发冻结指令，那么用户的所有资金操作都不被允许。   
   
Q：会员中会员和支付会员，两套单独维护？    
A：淘宝账户和支付宝账户应该不是一个吧。   
   
Q：大家怎么看待指纹，不说手机上验的有多可靠，只说对服务端来说指纹就等同于免密，怎么宣传上都把指纹看作是个无比安全的东西。   
A：指纹确实比较安全，但是由于是手机黑盒，所以对于我们来讲，我们没有办法防止苹果伪造指纹。手机root了也可以修改指纹，毕竟返回的只是true和false。   
   
Q：一个或多个用户对应一个支付会员中多个用户怎么理解的   
A：有些公司的策略不同 有些是按照自然人来看的 有些是业务线不同账户 但是支付时是一个的。   
   
Q：那么那种在途交易的资金那样你们会怎么处理？是会原路返回么？还是会在中间户？ 回答：我一般放在中间户   
   
   
## 自由讨论   
   
PM1：	账户会有账户类型   
P2：	比如风控系统识别出近期行为接近危险的会员 预先在登录时就要求验证 有这种流程没   
P3：	首先感谢分享，会员中的会员，和支付会员的具体区别场景，能不能再列举下   
P4：	自然人在不同商户下的支付动作   
P4：	应该在第三方支付中对应不同的会员吧   
P5：	会员的黑白灰名单机制是在支付会员系统中么   
P6：	我的理解，会员就是客户，一个客户有多个登录账户也就是用户，一个用户又有多个记账账户   
P5：	还是常规的会员系统里面   
PM1：	@龚正 就是你们遇到风控监控异常的时候，会对交易进行冻结，还是会对会员整体的进行异常处理。如果冻结了会员，还会影响正常业务不？交易的资金会走到其他户里还是怎么处理，可以讲下这些么？   
P7：	@P6 我的理解，会员就是客户，一个客户有多个登录账户也就是用户，一个用户又有多个记账账户   
P7：	我们也是这样理解的   
P3：	会员中会员和支付会员，两套单独维护？   
P7：	客户、用户   
P8：	类似司法冻结了 那   
P9：	[玫瑰]   
P10：	大家怎么看待指纹，不说手机上验的有多可靠，只说对服务端来说指纹就等同于免密，怎么宣传上都把指纹看作是个无比安全的东西   
P11：	一个或多个用户对应一个支付会员中多个用户怎么理解的   
   
P2：	会员对应到实名的人 只是个记录信息 实际操作和业务发生在登录帐号上   
PM1：	@龚正，那么那种在途交易的资金那样你们会怎么处理？是会原路返回么？还是会在中间户？   
P8：	问个支付会计的问题：到会计落分录，听大家说一般 是业务属性+支付账户属性 来确认落到什么科目，你们这层到科目是怎么做映射的？   
P10：	@龚正?，对啊返回的只是true、false。对于网络报文来说，只能依赖客户端不被破解，本质和无密也差不多   
P3：	淘宝账户和支付宝账户应该是打通或者一样的吧。如果单独维护，两套体系会产生一个议题，就是会不会涉及到信息同步的问题？或者说，有些信息，比如userId应该是一样的，还有实名认证信息，是共享的。   
P11	[强]感谢ark的分享和解答   
PM1：	[强]感谢ark的分享和解答   
P6：	支付宝和淘宝不是一个，只是绑定关系   
P12：	淘宝账户和支付宝账户 一个是业务的 一个是底层的   
P15：:	联合登录后在库中是怎么存的，这块能说说么   
P8：	@龚正 账户记账映射到科目 是怎么做的   
P10：	淘宝账户和支付宝账号不同，我猜是个悲伤的故事，不知道有没有阿里的人   
龚正：	联合登录后在库中是怎么存的，这块能说说么 联合登录是什么意思   
P6：	支付宝和淘宝是两个体系，只是账户打通   
P10：	谢谢分享   
   
   
龚正：	账户记账映射到科目 是怎么做的 在账户中存科目呗   
龚正：	[阴险]   
P16：	淘宝只管订单方面，支付宝只管支付方面的，这个不冲突吧   
P8：	哈哈   
P6：	联合登录是一种授权登录   
龚正：	淘宝账户代表的是电商相关的资产 支付宝账户代表自己资产   
龚正：	资金资产   
P8：	账户中直接存了科目？   
P12：	支付宝服务对象不只有淘宝 是面向全行业的商家 大家不要搞混淆了   
P8：	支付宝是自己的 客户-账户   
P17：	淘宝和支付宝做的应该是账户互通   
P6：	淘宝是阿里巴巴的，支付宝是浙江蚂蚁金服的   
龚正：	其实我感觉联合登陆和微信登陆 微博登陆等等差不多吧   
龚正：	多个对应一个   
P12：	支付会员的场景 只有会员支付吗？   
P3：	好的，学习了。   
P18：	OAuth2.0 认证授权 挺流行的吧   
P19：	oauth严格意义没认证 只是授权   
P19：	目前最好的解决方案了   
P10：	阿里、支付宝都是一家，淘宝可以用支付宝登录。我行用户体系被强制统一，理由之一就是阿里两套用户带来许多麻烦   
P6：	是一样的，用户在微信登录时再在别的系统登录，传密文到目标系统，目标系统找到映射用户号，查出相关信息，存入缓存   
P2：	会员是身份证号 帐号是手机号 业务都发生在帐号上 要封号应该从会员上封   
P20：	淘宝和支付宝账号也没打通吧？还是需要相互授权吧？   
P15：	联合登后和自有的用户是分开存的吧？   
P16：	OAUTH2.0就是单点登录登录的一种，不用区分是哪家企业的   
P21：	淘宝和支付宝账号是分开的 有一套映射规则 淘宝uid是底层基础库的标识   
P16：	你在网易云音乐照样可以用微信登录，只要去微信那边注册下就行了   
P6：	联合登录就是一张映射表   
P20：	OAUTH2.0接入时已经区分接入的是哪家企业了   
P8：	@P10 “我行用户体系被强制统一” 能否介绍下这个   
P19：	oauth联合登陆 只是授权登录信息 这算最基础的应用了   
P22：	淘宝和支付宝是绑定关系，且支持多对一的绑定   
P20：	oauth最终是获取accesstoken，授权只是第一个阶段   
   
   
P19：	银行都建有统一会员系统吧   
P6：	银行是cif   
P22：	各位是怎么处理金融和支付账户的   
龚正：	[动画表情]   
P18：	支付会员由于人行监管问题，等级上明显要高于电商会员，通常高等级向低等级上授权， 一个电商会员去了支付系统，没各种实名认证，啥也不能做。   
P2：	风控统计这些要考虑会员下所有帐号了 至于相同会员不同帐号共享登录这些根据不同公司喜好吧   
P22：	@龚正?比如信贷业务和支付账户的关系有什么建议吗   
P23：	这些会员和电商会员区别在哪里   
龚正：	信贷一般是自然人为基准吧   
P19：	会员系统 和支付系统 之间 登录统一授权就好了   
   
P6：	信贷支付两个业务，支付账户用来处理资金转移通道，如提现，还款   
P19：	建立会员系统 和授权中心 通用授权的注册一次性授予 其他的单独授权也可以   
P19：	有了这个 多少系统 都是一样的吧   
P22：	感觉这样容易出问题，我们现在好几款信贷产品，账户没打通，结果部分客户出现了多头负债@P6?@龚正?   
P22：	当然也有可能是单个自然人没有最高限额导致的[捂脸]   
P20：	肯定是借贷记账不平导致的??   
P24：	淘宝和支付宝是绑定的关系，可随时解绑和环绑，没有打通。   
P24：	![20170515_203416](http://wechat.lixf.cn/img/20170515_203416.png)   
P6：	信贷是基于客户的，应先建客户系统，全业务系统共享客户系统   
P20：	是的，都是独立的   
P25：	信贷产品之间互相的关联关系也有问题   
P22：	谢谢几位，看来我想复杂了   
P26：	@龚正?请问现在指纹支付这块，指纹数据都是存在本地，服务端只能授信于硬件，除了授信之外，有没有其他办法保证指纹数据正确？谢谢   
P6：	信贷产品挂在客户身上   
龚正：	指纹关键设备   
龚正：	并判断手机是否root   
P24：	金融和支付账户打通会有很多麻烦，监管对支付账户的各种要求会导致金融产品也得被迫「合规」改造，建议采用绑定方式。   
龚正：	目前也只能这样了   
P22：	@P6?目前是这么做的   
P26：	谢谢   
P2：	风控应该控制会员而不是帐号 一个会员小有多个帐号   
P18：	会员就是一套系统的用户体系，电商系统、支付系统、P2P系统一般都独立会员体系，登录账户可以共享，业务上差别很大的，拆开来比较合适，这样就不会人行支付监管需求，要影响P2P系统，完全共用的话，就相互影响咯。   
P6：	那就是授信问题了   
   
P27：	开始说到在账户中存科目，存的是一级科目吧，后面做总分对象平衡用到，这么理解不知道对不对？   
龚正：	存的是末级科目   
P6：	我们以前的会员体系是分业务的，用户分主副用户，副用户可以用主用户密码登录，用付用户做业务   
P10：	判断手机是否 root不够，因为请求可能根本没来自合法的客户端，当然这又是另外一个很大的话题   
P28：	设备指纹   
P24：	指纹支付对风控要求比较高，服务器端要验证 设备指纹，IP等客户信息，防伪造，同时要保证网络传输的安全性，防篡改。   
P28：	对的   
P12：	[强]   
P18：	一个账户的正常资金和冻结资金 你们一般怎么设计的？ 一条记录， 还是分开？   
P28：	一个用户有多个账户   
P2：	一会员多帐号这样会大大增加系统的复杂度 实名认证后应该合并成一个帐号 其实最终也是方便用户   
P28：	一个用户对应多个账户   
P28：	每个账户操作 都会对应相应的分录   
P2：	可以保留登录用户名 登录后操作都在应该帐号上   
P6：	账户的冻结解冻是有登记簿来管理的   
P6：	一会员多账户，账户实名时只实名当前账户，别的账户需要归并或签权合并，才能合到同一会员下   
P29：	支付系统中叫会员合适还是叫客户合适？   
P30：	会员   
P2：	允许多帐号实际上是破坏了关系数据库的范式约定 呵呵 不实名应该不允许产生业务数据 没实名前的帐号系统应该预留会员关联位置   
P29：	会员比客户含义貌似宽泛很多   
P6：	支付宝的会员含个人客户和商户，央行的客户指个人或买方   
P6：	不实名也应该能做业务   
P2：	如果帐号下已经跑了业务 那么关联数据会分散在各个地方 合并时风险就大了   
P6：	业务是跟着账户的，没问题   
P31：	你们所谓的一会员多账户是什么意思，能不能举个例子   
P29：	余额 余额宝   
P6：	一客户多用户，一个人有多个支付宝   
P2：	我说的是理想状态 实名现在有快捷途径操作很容易了 用户有能接受 这样减轻系统复杂度   
P11：	那怎么判断多个支付宝对应一个人   
P6：	理想是这样的，流程往往是业务说了算啊   
P29：	可以用一份实名认证吧   
P29：	支付宝是这样的   
P31：	一个人有多个支付宝？跟一账户多用户有什么关系，在银行卡没改制之前我一个银行也有多张银行卡，关键是系统也不见得把我分成一个人呀，都是一对一的关系   
P11：	即使实名的话，在数据库中认定也是不能体现的   
P11：	要根据唯一标识查询才能得到这个结果了   
P6：	银行肯定是一对多的   
P2：	风控就有漏洞了 前面敦煌那个人也是   
P6：	银行要cif就是干这个的   
P31：	问题是这玩意你们认为的那种一对多有什么好处？   
P31：	就好像我在这张银行卡猛消费，跟我另外一张银行卡有什么关系   
P31：	在银行卡没改革之前   
P6：	是和你本人有关   
P6：	客户是现实自然人在系统中的建模   
P31：	有什么关系，这个资金也不互通，积分也是，活动也是，想不出有什么关系   
P6：	信用   
P6：	授信，风控都会参考这些   
P6：	还有就是客户行为分析   
P31：	那如果你们搞这种一账户多用户的，系统里面单账户余额就是所有用户总额咯   
P31：	错了，是一会员多账户，会员余额就是多账户总额？   
P2：	业务可以存在多个帐号 但第一级关联必须是会员 之后二级关联到帐号 也没问题 说的是理想状态 不需要合并 但必须明确主体关联   
P6：	当然还有更多，可以这么说:相同姓名+身份证号视为同一个人，不论在哪个系统里，都是现实中的你，你在中行上了黑名单，招行也不会给你做业务   
P29：	余额好像一般是分开的，额度是一起共享的   
P6：	余额是另一个概念，资金账户   
P6：	额度是会员的资金账户，余额是用户的资金账户   
P32：	想请教下支付会员下会有哪些账户分类，分类的标准一般会有啥   
P31：	这个额度跟余额有什么关系没有   
P31：	还有这个额度代表什么，最高限额？   
P6：	我们先把概念统一了。 额度就是授信，类似于信用卡额度   
P29：	会员是身份证号，用户是身份证+手机号？   
P32：	在支付系统应该是限额，在消金领域即有限额又有授信   
P31：	哥们你一口气说完吧，我就看你的了，这些名词说实话每个人都不一样，我就看看你怎么说，按你标准理解   
P32：	估计不会这样，因为现在手机号就只能实名认证一张身份证   
P6：	用户一般用手机号区分   
P29：	@P6?我的理解对吗   
P32：	用组合标志去标识一个用户，拓展可能受限制   
P6：	等一下，我整理一下   
P2：	有业务就有风控要求 而风控对应会员 所以有业务前需要做实名认证   
P6：	我们的个人会员系统分三层:客户，用户，账户，客户就是一个自然人建模，用户常指一个注册用户，即系统使用者，也叫登录账户，账户，指存放资金的实体，用货币来计量   
P6：	客户通常通过其用户来使用系统，比如一个手机号注册的用户   
P29：	那会员这个概念呢？等同于客户吗   
P6：	对， 一个人有多个手机号，也就导致了同一个人在一个平台有多个用户   
P6：	一般是先有用户再有客户，用户通过实名认证产生客户，一个客户在系统中只有一个唯一标识:客户号   
P29：	明白了   
P6：	两个用户实名，如果证件号和姓名相同，我们认为是同一个客户下的两个用户在做实名   
P6：	第一个用户没问题，一对一产生了客户，当第二个用户实名时，由于客户已经存在，不能再创建了，或者说即使创建了也要合成一个，我们称为归并   
P29：	支付密码是在用户纬度是吗   
P2：	反正业务数据产生前必须找到客户 否则第一笔业务都可能产生风险 多个帐号没问题 加个登录用户也没关系 主要是业务安全上考虑   
P6：	可以在用户上。 归并一般是这样做的:当第二个用户实名时，系统检测到客户已经创建，会让第二个用户输入已实名用户的支付密码来进行签权归并   
P6：	支付宝以前是只有当你提现时才让你找客户，毕竟用户体验也要考虑   
P29：	现在用户发起交易的前提必须实名吗？   
P6：	我接着说归并，当第二个用户密码通过后，会把第二个也挂在此客户下，即:将客户号填入当前用户域中   
P6：	实不实名要看业务，也要看监管   
P2：	说影响体验看个人理解吧 除非跑的是无关紧要的数据 要不也是对客户不负责任[呲牙]   
P6：	基本上就这些吧，比较简单的。 从管控角度上说 客户冻结了，其下所有用户禁入，用户冻结了，用户下所有账户禁入   
P6：	一个原则:宽进严出   
P29：	[强]感谢   
P6：	你们聊吧，我看会黄金现货   
P2：	客户用户帐号之间就是两种关系表 业务表上存帐号id 统计就麻烦了   
P6：	业务表上同时存两个id   
P2：	客户的吗 用户没意义的 就是登录用   
P6：	都存，用户当然有意义了，你的操作是基于用户的   
P2：	再说吧 从关系表可以查到用户 用户可以看做是客户一个属性 无意义 有空聊吧 呵呵   
P6：	你考虑一下一个客户多用户时场景吧   
P6：	而且账户是在用户下的……   
P9：	其实最简单的我就是现在银行的系统下归集所有的银行卡的信用卡   
P31：	你那句会让已实名用户输入支付密码来进行归并是什么意思   
P31：	同一会员不同用户必须支付密码一样？还是说什么   
P6：	归并是要有验证的，否则我知道了你的证件，把自己用户挂你名下，如果你名下有信贷，钱就容易被我拿走。   
P6：	同一会员不同用户密码应该不一样   
P2：	知道 用户除了登录用处不大 业务已经关联帐号id了 这时的用户只是客户的暂时代表 在没实名前 实名后从关系可以找到客户那才是有用 业务要么多存客户id 要么不存就只有帐号id也可以 个人理解 数据存了终究要怎么用 风控时定位都用户还不够 要找到客户才行 不说了   
   
   
P8：	群里有没有做过资产证券化的？   
P6：	p2p么？   
P8：	信贷 ABS业务   
P33：	我·行·正在做ABS   
P8：	@P33    
P31：	Abs最好套个资管计划，不然资金池很稳定   
   
   
P31：	用户密码不一样但是支付密码一样？   
P6：	不一样，只有你知道另一个用户的密码的时候，才能确认另一个用户也是你   
P34：	在途资金、冻结资金、可用资金，需要通过多账户方法来实现吗？   
P2：	用户是虚拟的 客户帐号业务才是真正实体   
P31：	你这个流程我大概了解了，那我能不能说你这玩意其实是根据参照物来看的   
P31：	比如在中国人民银行看来的用户在商业银行看来可能是会员   
P20：	@P34?不需要多账户，账户中有账户余额，可用金额和冻结金额，账户余额=可用金额+冻结金额，一般只有出账账户需要冻结金额，冻结额度会存在一个冻结单，记录冻结的哪笔交易，哪个账户，冻结金额，冻结状态等，同时更新账户可用金额和冻结金额，交易成功做解冻出账，否则做解冻处理，恢复可用金额   
P34：	如果一笔交易，T日更新余额（在途状态），T+1转可用，如何在账户层面实现在途转可用的过程呢？   
P19：	余额 是 好几个值： 可用余额、 未确认余额、 冻结余额。当前 余额 是 这几个的总和。   
P20：	我认为在途金额处理方式跟冻结金额是一样的，在途金额转可用首先是这笔交易的最终状态肯定是确定的，要么成功要么失败   
P34：	如果通过支付账户挂子账户的方式实现？是不是很啰嗦？区分在途资金账户、冻结资金账户、可用资金账户。可用余额=可用资金账户。不可用余额=在途资金账户+冻结资金账户；总余额=可用+不可用   
P19：	有很多处理方法   
P6：	在途资金不应该和余额统一处理   
P34：	在请教问题：管理办法支付公司不允许为证券、信托等开户。   
P19：	有些交易是依赖冻结的 有些依赖中间账户   
P34：	那可否有业务往来？资金如何处理？   
P6：	余额是指已到账不可撤消的资金   
P34：	这个是呀   
P31：	民生哥们，我刚刚的比喻对不对   
P6：	差不多吧   
P31：	支付公司是尽量别跟那些玩意打交道，不然死的快，特别是证券[捂脸][捂脸][捂脸][捂脸]   
P20：	@P34?在途资金我刚才说法有误，请@P6?帮忙解答下[抱拳]   
P6：	余额和在途不是一个维度   
P6：	我想知道业务场景   
P6：	如果一笔交易，T日更新余额（在途状态），T+1转可用，如何在账户层面实现在途转可用的过程呢？   
P34：	代扣一笔，支付确认实时。   
P6：	是这个吧   
P34：	t+1，资金到备付金账户，转可用   
P34：	如何在账户层，实现资金在途到可用的变化捏？   
P34：	嗯那   
P18：	在途一般在中间户体现   
P35：	一个账户内设两个子账户，一个现金，一个在途   
P34：	看来每个公司账户设置都不一样啦[偷笑][偷笑]   
P34：	通用方案，或者说“准标准”方案，是啥咧？   
P36：	你定的在我眼里就是标准的   
P18：	供参考，一笔收单涉及2个结算，银行T+1结算： 渠道待清算账户（在途） -》 银存账户（备付金余额）； 商户T+1结算：结算中间户（在途）-》 商户结算账户（余额）；   
P34：	[呲牙][呲牙][呲牙][呲牙][偷笑][偷笑][偷笑]   
P6：	关键是有没有特殊处理   
P6：	你说的场景还是不是很清楚   
P20：	商户结算账户是不是就是在途资金账户？只有t+1结算账户金额被转到余额账户才能操作   
P36：	本质在于 我们给商户结算 是否应该依赖于通道方给我们结算   
P6：	不应该   
P36：	如果通道方没给我们结算 但是到了我们给商户结算的时间点 我们不想自己垫资给商户……   
P6：	这是两笔账   
P36：	这就是她的需求   
P36：	嗯 我也认为两者应该分开   
P6：	合同呢？   
P18：	信息流和资金流本来就是分开的。。   
P6：	如果通道不给你们结，你们永远不给商户结？   
P36：	现状是 通道方t+1结算给我们 我们跟商户的合同也是t+1 然后我们计算商户手续费 还要依赖于通道的对账文件   
P36：	嗯 如果通道没结 就先去追钱……因为额度太大 垫不起   
P6：	流程有问题   
P18：	垫资是因为这2个之前差异造成的。比如商户T0 银行T1   
P36：	嗯 应该完全隔离 通道和商户对吧   
P6：	对账流程有问题   
P36：	或者把商户结算周期拉长 或者自己垫资 就不会这么痛苦了   
P34：	如果有好的渠道可实时识别类别，可提前扣，不依赖于对账文件   
龚正：	一般都是商户周期很长啊   
P6：	对，对商户你们要自主对账，对于通道，以通道为主   
P34：	俺们特殊[呲牙]   
龚正：	厉害   
P36：	业务场景决定我们不能留钱……   
P38：	个人认为这个的记账完全根据业务来，在电商业务的余额体系里面，用户充值，支付渠道返回成功交易结果后，就该给用户显示余额。普通电商此时都不会有在途资金账户。高级一点能有这个账户。   
P36：	说白了 就是业主着急要钱！   
龚正：	着急要那为啥过你们。。[憨笑]   
P6：	分开处理就对了   
龚正：	还走第三方   
P6：	流水好看啊   
P34：	嗯嗯。   
龚正：	你们是房产交易吗   
龚正：	这种交易如果过第三方 时间是个问题啊   
P36：	是先过户 还是先给钱 ～我们就解决这个问题客户先拿出钱给我们就过户 过户后就给钱到业主   
P37：	房地产交易的支付宝   
P6：	分开处理，日终清算时，你们同时算好通道手续费及应收备付金，商户手续费及结算资金，对于双方都是对账打款，差错后期处理   
龚正：	厉害   
P36：	嗯 以后肯定要规范到这种正规流程   
龚正：	@小北-理房通-资金?你们自己是第三方呗   
P34：	嗯   
P6：	给通道方送个礼，上午给你们打款，你们下午打给业主   
P34：	[呲牙]   
P36：	[动画表情]   
龚正：	[动画表情]   
龚正：	房产的特点是客单量小 客单价大   
龚正：	普通电商的套路确实有点搞不定啊   
P36：	系统压力比你们小多了 我们可以慢点 ～不出资损就好   
龚正：	哈哈 要不你们就快一天 多收点手续费啥的   
龚正：	有垫资风险 就多点风险收益   
龚正：	[动画表情]   
P36：	木钱～   
P38：	T+0流水贷，提前结算   
P8：	账户中有账户余额，可用金额和冻结金额，账户余额=可用金额+冻结金额，一般只有出账账户需要冻结金额，冻结额度会存在一个冻结单，记录冻结的哪笔交易，哪个账户，冻结金额，冻结状态等，同时更新账户可用金额和冻结金额，交易成功做解冻出账，否则做解冻处理，恢复可用金额   
P6：	如果是这种情况，就用在途资金账户，因为一旦计入余额，就会纳入资产类，没人备付金，你纳入资产就有问题了   
龚正：	流水贷是啥意思啊   
龚正：	[惊恐]   
P34：	“银行系流水贷”？？？   
P8：	看到这个回答，记得还有一套类似模型。可用余额、预冻结金额、未达金额 、系统中金额   
P38：	@龚正?基于交易流水的贷款，也算是应收帐款贷款，同时基于企业资质。通常由收单支付公司或者合作资产方提供。   
P36：	学习了   
龚正：	奥 这样啊   
P32：	供应链金融？   
龚正：	厉害啦   
P8：	系统中金额用来处理A转给B 同时B转账给C   
龚正：	才看到你是ping++的   
龚正：	[色]   
P6：	应收账款的扺压贷款   
P38：	和供应链金融性质形似；流水贷是支付公司尝试的增值业务。   
P31：	你玩这种风险太大，个人建议小心为好   
P31：	你这种不是供应链金融，是信用贷款   
P6：	都有   
P31：	供应链金融必须有明确的标的，要么是应收账款类型，要么是预付款，要么存货，他这种流水贷其实跟阿里的借呗没啥区别   
P6：	不是有扺押么？纯信用？   
P38：	资方和第三方支付公司合作，或者第三方支付公司自己做，风险是很小的。原本通过第三方支付公司收单的资金T+1结算给商户，商户在第三方支付公司这开通流水贷，T+0就拿到对应的结算资金；对第三方支付公司而言，就是基于成功交易的交易流水提前一天向商户结算资金。   
P31：	不懂，我就往前反了一下，没看全   
龚正：	这种贷款一般问题不大   
P34：	您说的是特约商户t0业务   
P6：	基于结算资金抵押   
龚正：	回笼资金挺快 不过小公司作假就悲剧了   
龚正：	还是看信用   
P25：	这个也叫贷款？   
P31：	哦，这个叫流水贷[捂脸][捂脸][捂脸]，这个不就是D0业务吗   
P6：	我们叫D0   
P25：	一脸懵逼[尴尬]   
P31：	你看看又是名词定义不一样的结果   
P31：	[捂脸][捂脸][捂脸][捂脸][捂脸]   
P34：	[呲牙][呲牙][呲牙]   
P34：	哈哈哈哈哈   
P28：	这对于第三方来说 就是贷了结算款 t+1第三方不给商户结算 是这意思么   
P6：	垫资D0结算   
P38：	[Facepalm][Facepalm]   
P25：	对商户来说提前结算是好事   
P18：	全支付公司自己垫资是D0，区别引入了其它资产提供方？   
P25：	但不会是便宜事吧   
龚正：	提前结算还是有风险的   
P38：	收费标准不一   
P25：	利息是多少   
P6：	手续费就高   
P25：	拿个标准来思考下   
龚正：	所以实力雄厚才垫资 要不就找放贷方 放贷同时又买了保险   
P6：	我知道的有10%手续费   
P25：	这种业务场景也是真实存在的   
P28：	这没啥风险吧   
龚正：	也有   
P18：	银行一般万五？   
龚正：	风险肯定还是有的   
P6：	有，上游不给结就是风险   
P28：	该结多少就贷多少还是每天给商户贷的都一样？   
P28：	上游不就是银行吗   
P18：	POS T0结算很多都这么干吧，商户自己出手续费   
P25：	这种对应到线下有没得类似的实际业务   
P6：	银行卡套现业务   
P25：	感谢，不过银行卡套现和这个还不是很贴合   
P6：	睡了，大家继续   
P18：	套现都是急着想拿到钱的…   
P36：	[月亮][月亮]   
P25：	不是很清楚商户付相对较高的手续费来要求T+0清算的需求根源   
P25：	[月亮][月亮]   
P8：	@P6?你们说的这种提前收款和保理模式的提前收款是一类么？   
P31：	不可能百分之十的哥们，最多百一百二顶天了，百十的那是洗钱   
P18：	商户T0实时代发，通过线上充值一般是要垫资的，可以商户直接银行转账，系统实现自动登账，都能省点。   
   
      
