## 作者信息
刘理彬
QQ:214434802

## 技术栈
vue2 + vuex + vue-router + vue-resource+ vue-lazy-render + webpack + ES6/7 + fetch + sass + flex + svg



# 项目运行

#### 注意：由于涉及大量的 ES6/7 等新属性，nodejs 必须是 6.0 以上版本 ，node 7 是先行版，有可能会出问题，建议使用 node 6 稳定版

```
cd jkd-weishop

npm install

```

### 编译环境
```
npm run dev

访问 http://localhost:8088
```


### 线上版本
```
npm run build

生成的web文件夹放在服务器即可正常访问
```




# 说明

>  本项目主要使用用 vue2 架构的一个项目

>  开发环境 macOS 10.12.3  Chrome 56  nodejs 6.10.0

>  图片懒加载插件安装 sudo npm install vue-lazyload

>  vue-resource 安装 sudo npm install vue-resource

>  vue-lazy-render 安装 sudo npm install vue-lazy-render

# 项目布局

```

├── build                                       // webpack配置文件
├── config                                      // 项目打包路径
├── web                                         // 上线项目文件，放在服务器即可正常访问
├── src                                         // 源码目录
│   ├── components                              // 组件
│   │   ├── common                              // 公共组件
│   │   │   ├── address.vue                     // 地址选择组件
│   │   │   ├── alertTip.vue                    // 弹出框组件
│   │   │   ├── computeTime.vue                 // 倒计时组件
│   │   │   ├── loading.vue                     // 页面初始化加载数据的动画组件
│   │   │   └── mixin.js                        // 组件混合(包括：指令-下拉加载更多，处理图片地址)
│   │   ├── footer
│   │   │   └── footGuide.vue                   // 底部公共组件
│   │   ├── header
│   │   │   └── head.vue                        // 头部公共组件
│   │   └── home
│   │       ├── imageAd.vue                     // 单图／轮播图组件
│   │       ├── imageNav.vue                    // 图片导航组件
│   │       ├── notice.vue                      // 公告组件
│   │       ├── product.vue                     // 商品组件
│   │       ├── richText.vue                    // 富文本组件
│   │       ├── searchForm.vue                  // 搜索框组件
│   │       ├── shop.vue                        // 店铺头部组件
│   │       └── product.vue                     // 商品组件
│   ├── config                                  // 基本配置
│   │   ├── env.js                              // 环境切换配置
│   │   ├── fetch.js                            // 获取数据
│   │   ├── mUtils.js                           // 常用的js方法
│   │   └── rem.js                              // px转换rem
│   ├── images                                  // 公共图片
│   ├── page
│   │   ├── cart
│   │   │   └──  cart.vue                        // 购物车
│   │   ├── confirmOrder
│   │   │   ├── children
│   │   │   │   ├── children
│   │   │   │   │   └── addAddress.vue          // 添加地址页
│   │   │   │   └──chooseAddress.vue            // 选择地址页
│   │   │   └── confirmOrder.vue                // 确认订单页
│   │   ├── home
│   │   │   │   └──  children
│   │   │   │     └── innerPage.vue             // 首页内页
│   │   │   └── home.vue                        // 首页
│   │   ├── order
│   │   │   ├── children
│   │   │   │   ├── logistics.vue               // 物流信息
│   │   │   │   └── orderDetail.vue             // 订单详情页
│   │   │   └── order.vue                       // 订单列表页
│   │   ├── paySuccess
│   │   │   └── paySuccess.vue                  // 订单支付成功页
│   │   ├── productDetail
│   │   │   └── productDetail.vue               // 商品详情页
│   │   ├── productSearch
│   │   │   └── productSearch.vue               // 商品搜索页
│   │   ├── profile
│   │   │   └── profile.vue                     // 个人中心
│   │   ├── search
│   │   │   └── search.vue                      // 搜索页
│   │   ├── service
│   │   │   └── service.vue                     // 售后
│   │   └── type
│   │       └── type.vue                        // 分类页
│   ├── plugins                                 // 引用的插件
│   ├── router
│   │   └── router.js                           // 路由配置
│   ├── service                                 // 数据交互统一调配
│   │   ├── getData.js                          // 获取数据的统一调配文件，对接口进行统一管理
│   │   └── tempdata                            // 开发阶段的临时数据
│   ├── store                                   // vuex的状态管理
│   │   ├── action.js                           // 配置actions
│   │   ├── getters.js                          // 配置getters
│   │   ├── index.js                            // 引用vuex，创建store
│   │   ├── modules                             // store模块
│   │   ├── mutation-types.js                   // 定义常量muations名
│   │   └── mutations.js                        // 配置mutations
│   └── style
│       ├── common.scss                         // 公共样式文件
│       ├── mixin.scss                          // 样式配置文件
│       └── swiper.min.css                      // 轮播插件
│   ├── App.vue                                 // 页面入口文件
│   ├── main.js                                 // 程序入口文件，加载各种公共组件
├── favicon.ico                                 // 图标
├── index.html                                  // 入口html文件
└── package.json                                // 项目构建配置文件