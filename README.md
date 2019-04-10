
# iOS Guide

* ## 关键字和语言特性的问题

    * [synthesize关键字的作用](lang_feature/synthesize关键字的作用.md)

    * [string属性用copy和strong修饰符时的不同](/lang_feature/string属性用copy和strong修饰符时的不同.md)
    
    * [属性修饰符`strong`、`weak`、`assign`、`copy`的作用](/lang_feature/属性修饰符分别的作用.md)
    
    * [`__weak`和`__block`的作用](/lang_feature/属性修饰符分别的作用.md?id=__weak和__block的作用)

    * 如何让自定义对象支持copy操作

    * `__block`在ARC和MRC下的作用一样吗
    
    * [`nonatomic` 和 `atomic`的作用](/lang_feature/属性修饰符分别的作用.md?id=nonatomic和atomic的作用)

    * atomic是线程安全的吗

    * [`weak`的底层实现原理](/lang_feature/weak的底层实现原理.md)

    * [`weak`属性如何自动置`nil`](/lang_feature/weak的底层实现原理.md?id=当weak指针指向的对象释放时，weak指针如何自动置为nil的)

    * `strong`的实现原理

    * [autorelease和autoreleasePool](/lang_feature/autorelease和autoreleasepool.md)

    * autoreleasePool的实现原理

    * 在子线程调用autorelease会如何

    * 如何定义私有属性和私有方法

    * [OC中类和结构体的区别](/lang_feature/OC中类和结构体的区别)

    * Category的特性

    * 为什么`Category`中不能添加属性

    * [`_Nullable`、`nullable`、`__nullable`等关键字的作用和使用](/lang_feature/nullable_keyword.md)

* ## Runloop

    * 什么是RunLoop，RunLoop的作用是什么

    * RunLoop在一个循环中是怎么做的，处理了哪些东西

    * RunLoop中有哪些东西

    * RunLoop和线程的关系

    * 系统基于RunLoop实现的功能

    * RunLoop的应用场景

        * 基于RunLoop的机制，优化tableView滑动流畅度
    
    * RunLoop间如何进行通信

    * 如何在RunLoop空闲的时候处理特定任务

* ## Block相关问题

    * [block的本质，以及clang对block的实现](/block/block的本质.md)

    * [block捕获变量值的原理。](/block/block值捕获原理.md)
        
        * 为什么block中使用的外部变量，当创建完block之后即使更改变量，block中的变量值也不会改变。
        
        * 为什么block中不可以更改外部变量的值。

    * [为什么block中静态变量、全局变量、静态全局变量的值可以更改](/block/block中全局变量等更改值的原理.md)

    * [有几种类型的block，block的存储区域](/block/block的存储区域.md)

        * 有几种类型的block，分别是怎么产生的

        * block属性是不是要用copy

    * [为什么__block修饰的变量值可以更改](/block/__block修饰符的作用和原理.md)

        * `__block`的底层实现

        * `__block`修饰的变量存储区域

    * [为什么block中的对象可以在对象的作用域之外使用。block截获对象的原理](/block/SAQ.md)

* ## Runtime

    * [消息转发机制](/runtime/消息转发机制.md)

* ## 多线程

    * 什么是GCD

    * 线程之间通信方式

    * 同步、异步、并发、串行的概念

    * 同步一定是在当前线程执行吗

    * 串行队列一定是只有一条线程去执行这个队列中的任务吗 / 将任务同步提交到一个串行队列为什么是当前线程执行

    * 什么是线程同步。实现线程同步的方式

        * 用锁

        * 串行队列

    * 用过哪些锁，哪些锁的性能比较高

    * 队列和线程的关系

    * GCD中API的作用和其应用场景

        * `dispatch_group`

        * `dispatch_barrier_async`

        * `dispatch_semaphore`

        * `dispatch_queue_create`

        * `dispatch_apply`

        * `dispatch_after`

* ## 系统框架和系统机制问题

    * ### 动画相关

        * 执行动画的几种方式

        * 动画是如何渲染显示的，哪条线程执行的动画

        * [UIView和CALayer的关系](/system_feature/UIView和CALayer的关系)

    * [iOS事件响应链和事件传递机制](/system_feature/iOS的事件传递链和响应链.md)

    * [iOS的drawRect方法和重绘机制](/system_feature/iOS的drawRect方法和重绘机制.md)

    * 使用drawRect有什么影响

    * [iOS的渲染机制和卡顿原因](/system_feature/渲染机制和卡顿原因.md)

    * ### KVO观察者机制

        * [KVO的实现原理](/system_feature/KVO/KVO的实现原理.md)

        * [KVO使用注意点](/system_feature/KVO/KVO使用注意点.md)

        * [如何关闭KVO和手动触发KVO](/system_feature/KVO/如何关闭KVO和手动触发KVO.md)

        * 重写了setter方法还会走KVO吗

        * [KVO的基本使用示例](/system_feature/KVO/KVO的基本使用.md)
    
    * ### [UITableView]

        * [为什么cell不从tableView的顶点开始布局](/system_feature/tableview_adjustinset.md)

    * ### [UIViewController]

        * [UIViewController常见问题](/system_feature/vc_faq.md)

        * [`UIViewController`布局相关的一些属性：`edgesForExtendedLayout`,`extendedLayoutIncludesOpaqueBars`,`automaticallyAdjustsScrollViewInsets`](/system_feature/vc_layout_property.md)

        * [控制器的视图加载和生命周期 / vc中的view什么时候创建 / loadView的作用 / vc init之后有视图吗](/system_feature/ViewController视图加载和生命周期.md)

    * ### [UITextField]

        * [UITextField常见bug]

    * [load方法和initalize方法](/system_feature/load方法和initalize方法.md)

    * 如何去设计一个通知中心 / 通知中心的实现

    * 为什么UI更新需要在主线程执行

    * appdelegate中的的回调都是什么时候触发

    * [UIImage是否是延迟解码的，什么时候进行的解码](/system_featurn/FAQ.md)

    * NSTimer的常见问题

        * NSTimer如何创建、如何销毁

        * timer的缺点和使用中容易出现的问题

        * 如何创建比较准的定时器

        * 如何在子线程中schedule一个NSTimer

        * 当APP进入后台之后，NSTimer还会继续执行吗。RunLoop会休眠吗

        * dispatch_source在页面退出之后会释放吗 NSTimer会释放吗

    * [通知的观察者在销毁的时候需要主动将自己从通知中心移除吗](/system_feature/remove_observer_from_notificationcenter.md)

    * [集合的遍历方式](/system_feature/集合的遍历.md)

    * [如何在遍历数组的时候删除元素](/system_feature/集合的遍历.md)

    * iOS中`NSString`的`hash`方法，只能比较96字节的字符。当字符串超过长度之后，取字符串的前32后32中32字符去进行比较。即只要这96个字符相同，那么字符串的hash值就会是相同的

* ## 开发笔记

    * [工程配置时的常见问题](/my_note/project_config_issue.md)

    * [RAC的最最基本使用](/my_note/RAC_base_use.md)

    ### 功能实现

    * [瀑布流的实现](/my_note/瀑布流的实现.md)

    * [下拉刷新的实现](/my_note/下拉刷新控件的实现思路.md)

    * [iOS中的单例模式实现](/my_note/singleton.md)

    * OC如何实现函数式编程语法

    * [实现网络请求的顺序执行及方案比较](/my_note/network_serial.md)

    * [AFNetworking与信号量使用时导致的死锁](/my_note/AFN_Semaphore_deadlock.md)

    ### 优化记录

    * [视图调试工具的使用](/optimize/视图调试工具的使用.md)

    * [流畅度优化记录](/optimize/流畅度优化记录.md)

    * [APP流量优化记录](/optimize/流畅度优化记录.md?id=流量优化过程记录)

    * [ipa包大小优化点记录](/optimize/ipa包大小优化点记录.md)

    * [组件化过程中私有Pod库优化过程记录](/optimize/pod_optimize.md)

    ### 工程管理

    * [通过Makefile统一团队中的工具版本]()

    * [开发规则和技巧](/my_note/开发规范和技巧.md)

    * [代码规范](/my_note/code_rule.md)

## 开发工具的使用

* [LLDB命令使用]()

*  [XCode缓存清理目录]()

* [`project.pbxproj `的解析及脚本修改证书配置思路实现](/assist_tool/project_pbxproj文件解析.md)

* [xcodebuild命令进行打包]()

* [XCode10下如何切换编译系统](/assist_tool/change_xcode_build.md)

* [`xcodebuild`使用旧版本编译系统](/assist_tool/change_xcode_build.md)

* [多XCode版本时更改`xcodebuild`使用的XCode版本](/assist_tool/change_xcode_build.md)

* [XCode快捷键](/assist_tool/xcode_keymap.md)

* [XCode Build Setting中的设置项](/assist_tool/)

* gitlab的自动化使用

	* 服务端hook的使用-实现提交代码后自动构建framework

	* pipelines的使用

	* Auto DevOps的使用

* ## 工程设计问题

    * [如何追踪crash，线上crash率的追踪]()

    * 如何进行crash保护。比如消息转发后找不到方法时避免崩溃。比如数组越界时如何避免crash。数组字典插入空值时通过setvalue方法允许插入空值操作。

    * 面向对象的设计原则：SOLID原则

    * 什么是简单工厂模式、工厂模式、抽象工厂模式

    * iOS中装饰器模式如何实现

    * iOS中的target-action机制

    * [iOS中的单例模式实现](/my_note/singleton.md)

    * 如何设计在本地缓存数据与服务端数据一致时,服务端不返回最新数据

        参考HTTP304状态码实现机制 ETag
    
    * [当设计一个模块或升级一个模块时需要考虑的内容](/my_note/module_design.md)

***

* ## 计算机基础问题

    * HTTPS通信过程

    * [TCP三次握手和四次挥手的过程](/basic_of_computer/TCP三此握手和四次挥手.md)

    * TCP怎样保证的可靠交付

    * DNS是基于TCP还是UDP的

    * 冒泡排序算法

    * 选择排序算法

    * 快速排序算法

    * 插入排序

    * 归并排序

    * 桶排序算法

    * 堆排序算法

    * 两个长字符，如何快速比较是否相同

## 知识扩展

* quic

* spdy

* grpc
