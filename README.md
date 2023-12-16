# WeChat-mini-program
基于微信小程序的面试宝典设计
#项目介绍

该项目为基于微信小程序的程序员面试宝典，旨在为广大用户提供高质量的面试资料和面试相关的实用信息，很大程度上帮助用户提高面试的水平。

核心功能介绍:

1.  岗位信息功能：用户首先通过此模块可以获取到所有正在招聘的公司的列表，列表中详细的介绍了各招聘公司的背景信息，用户可以通过自身需求点击对应的公司，获取到该公司招聘的岗位，要求条件,薪资待遇等各类详细信息。
2.  IT资讯，新闻功能：用户首先可以在面试宝典中去浏览比较实时的IT资讯，新闻的列表，然后用户根据自己兴趣点击某个标题已查看对应的详细内容。
3.  面试题目功能：用户在不同题型分类下获取到自身所学的题目题干，点击对应题目得到改题目的详细答案。
4.  面试题目预测功能：用户可以获取到由系统根据一定规则所给出的题目预测题干列表，用户可以根据需求获取对应题目的答案。
5.  在线客服功能：用户可以与小程序的客服人员进行在线交流。
6.  意见反馈功能: 用户可以根据自己的使用感受利用此功能向开发者提供宝贵的建议和反馈，以便开发者在后期进行对产品的优化和改进。
7.  论坛功能:  用户可以在论坛发布一些帖子，其中包括图片，视频，文字地理位置等信息，同时也可以对他人发布的动态进行评论，点赞，转发。



其中1-6项功能后端逻辑是在Gdesign中实现，第7个功能的后端逻辑在friends项目中完成

前端设计均在Gdesign-qian中完成



#开发环境

1. 开发工具：

​      IntelliJ IDEA 2022.2，微信开发者工具

​      Java-jdk1.8

​      Mysql 8.0

2. 依赖：

   Gdesign中需要用到的依赖:

   ```
   <dependencies>
       <dependency>
           <groupId>org.springframework.boot</groupId>
           <artifactId>spring-boot-starter-web</artifactId>
       </dependency>
   
       <dependency>
           <groupId>org.springframework.boot</groupId>
           <artifactId>spring-boot-devtools</artifactId>
           <scope>runtime</scope>
           <optional>true</optional>
       </dependency>
       <dependency>
           <groupId>com.mysql</groupId>
           <artifactId>mysql-connector-j</artifactId>
           <scope>runtime</scope>
       </dependency>
       <dependency>
           <groupId>org.projectlombok</groupId>
           <artifactId>lombok</artifactId>
           <optional>true</optional>
       </dependency>
       <dependency>
           <groupId>org.springframework.boot</groupId>
           <artifactId>spring-boot-starter-test</artifactId>
           <scope>test</scope>
       </dependency>
       <dependency>
           <groupId>com.baomidou</groupId>
           <artifactId>mybatis-plus-boot-starter</artifactId>
           <version>3.2.0</version>
       </dependency>
       <dependency>
           <groupId>org.springframework.boot</groupId>
           <artifactId>spring-boot-starter-freemarker</artifactId>
       </dependency>
   
   </dependencies>
   ```

​     

​        friends中所用到的依赖：

```
<dependencies>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-test</artifactId>
        <scope>test</scope>
    </dependency>


    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter</artifactId>
    </dependency>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-web</artifactId>

        <!-- <exclusions>
          <exclusion>
              <groupId>org.springframework.boot</groupId>
              <artifactId>spring-boot-starter-tomcat</artifactId>
          </exclusion>
      </exclusions> -->

    </dependency>

    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-configuration-processor</artifactId>
        <optional>true</optional>
    </dependency>



    <!-- apache 工具类 -->
    <dependency>
        <groupId>commons-codec</groupId>
        <artifactId>commons-codec</artifactId>
    </dependency>
    <dependency>
        <groupId>org.apache.commons</groupId>
        <artifactId>commons-lang3</artifactId>
        <version>3.7</version>
    </dependency>
    <dependency>
        <groupId>org.apache.commons</groupId>
        <artifactId>commons-io</artifactId>
        <version>1.3.2</version>
    </dependency>

    <!-- httpclient -->
    <dependency>
        <groupId>org.apache.httpcomponents</groupId>
        <artifactId>httpclient</artifactId>
    </dependency>


    <!-- db driver -->
    <dependency>
        <groupId>mysql</groupId>
        <artifactId>mysql-connector-java</artifactId>
        <version>8.0.30</version>
    </dependency>

    <!-- mybatis -->
    <dependency>
        <groupId>org.mybatis.spring.boot</groupId>
        <artifactId>mybatis-spring-boot-starter</artifactId>
        <version>1.3.1</version>
    </dependency>
    <!--mapper -->
    <dependency>
        <groupId>tk.mybatis</groupId>
        <artifactId>mapper-spring-boot-starter</artifactId>
        <version>2.0.3</version>
    </dependency>
    <dependency>
        <groupId>tk.mybatis</groupId>
        <artifactId>mapper</artifactId>
        <version>4.0.3</version>
    </dependency>
    <!--page helper -->
    <dependency>
        <groupId>com.github.pagehelper</groupId>
        <artifactId>pagehelper-spring-boot-starter</artifactId>
        <version>1.2.3</version>
    </dependency>

    <!-- swagger2 配置  /swagger-ui.html -->
    <dependency>
        <groupId>io.springfox</groupId>
        <artifactId>springfox-swagger2</artifactId>
        <version>2.4.0</version>
    </dependency>
    <dependency>
        <groupId>io.springfox</groupId>
        <artifactId>springfox-swagger-ui</artifactId>
        <version>2.4.0</version>
    </dependency>

    <!-- 更加美观的swagger2 ui   /doc.html-->
    <dependency>
        <groupId>com.github.xiaoymin</groupId>
        <artifactId>swagger-bootstrap-ui</artifactId>
        <version>1.6</version>
    </dependency>



    <!-- 微信拿到用户的手机号 -->
    <dependency>
        <groupId>org.bouncycastle</groupId>
        <artifactId>bcprov-jdk15on</artifactId>
        <version>1.60</version>
    </dependency>

    <dependency>
        <groupId>javax.persistence</groupId>
        <artifactId>javax.persistence-api</artifactId>
        <version>2.2</version>
    </dependency>

    <dependency>
        <groupId>com.qcloud</groupId>
        <artifactId>cos_api</artifactId>
        <version>5.6.8</version>
    </dependency>
</dependencies>
```

​        

#目录结构描述

**Gdesign的目录结构**

│  Gdesign.iml
│  mvnw
│  mvnw.cmd
│  pom.xml                //pom配置文件，导入项目依赖 
│
│
├─src
│  ├─main
│  │  ├─java
│  │  │  └─com
│  │  │      └─example
│  │  │          └─gdesign
│  │  │              │  GdesignApplication.java      //程序运行入口，负责扫描mapper层
│  │  │              │
│  │  │              ├─config
│  │  │              │      MybatisPlusConfig.java    //Mybatis配置文件
│  │  │              │
│  │  │              ├─controller  //项目控制层，调用业务层方法来控制业务逻辑
│  │  │              │      AnwserController.java  //用于面试题目功能中，查询对应面试题目的答案
│  │  │              │      CompanyController.java   //用于在岗位信息功能中，查询到所有招聘公司的详情并返回数据
│  │  │              │      EmploymentController.java  //用户岗位信息功能中，查询每个招聘公司对应的招聘岗位信息
│  │  │              │      InforListController.java   //用于IT资讯，新闻功能中，查询所有资讯，新闻的标题列表
│  │  │              │      InformationController.java //用于IT资讯，新闻功能中，查询对应标题下详细资讯新闻信息
│  │  │              │      MainfController.java  //用于返回该项目所有功能的名称集合给前端
│  │  │              │      SwiperController.java  //用于查询数据库并返回前端页面轮播图地址信息
│  │  │              │      TitleController.java    //用于面试题目功能中，查询所有面试题目分类列表，还会记录题目点击次数
│  │  │              │      TitletypeController.java  //用于面试题目功能中，查询该分类下所有题目题干
│  │  │              │      UserController.java //用于获取用户登录时用户名与密码
│  │  │              │
│  │  │              ├─dao // 各个文件对应本身的业务层，业务层调用Dao层来实现与数据库的交互
│  │  │              │      Anwser.java
│  │  │              │      Company.java
│  │  │              │      Employment.java
│  │  │              │      Forumlist.java
│  │  │              │      Inforlist.java
│  │  │              │      Information.java
│  │  │              │      Mainf.java
│  │  │              │      Swiper.java
│  │  │              │      Title.java
│  │  │              │      Titletype.java
│  │  │              │      User.java
│  │  │              │
│  │  │              └─mapper //各个文件对应本身的控制层，被控制层调用。
│  │  │                      AnwserMapper.java
│  │  │                      CompanyMapper.java
│  │  │                      EmploymentMapper.java
│  │  │                      ForumlistMapper.java
│  │  │                      InforMapper.java
│  │  │                      InformationMapper.java
│  │  │                      MainfMapper.java
│  │  │                      SwiperMapper.java
│  │  │                      TitleMapper.java
│  │  │                      TitletypeMapper.java
│  │  │                      UserMapper.java
│  │  │
│  │  └─resources
│  │      │  application.yml   //与本地数据库相连接的配置信息
│  │      │
│  │      ├─Mapper
│  │      ├─static
│  │      └─templates
│  └─test
│      └─java
│          └─com
│              └─example
│                  └─gdesign
│                          GdesignApplicationTests.java
│



**friends目录结构**

│  .gitignore
│  friends.iml
│  HELP.md
│  mvnw
│  mvnw.cmd
│  pom.xml    //加载项目依赖文件
│
│  └─libraries //加载maven依赖
│      
│
├─src
│  ├─main
│  │  ├─java
│  │  │  ├─com
│  │  │  │  └─project
│  │  │  │      │  ProjectApplication.java  //程序入口
│  │  │  │      │  Swagger2.java   //用于restful风格的Web服务
│  │  │  │      │  WarStartApplication.java
│  │  │  │      │  WebMvcConfig.java  //MVC框架配置文件
│  │  │  │      │
│  │  │  │      ├─controller  //项目控制层，调用业务层方法来控制业务逻辑
│  │  │  │      │  │  ActionsController.java  //用于论坛功能中发表帖子，获取用户所有帖子详情，发布帖子，删除帖子，发表评论，删除评论的功能
│  │  │  │      │  │  HelloController.java 
│  │  │  │      │  │  UserController.java //用于用户登录
│  │  │  │      │  │
│  │  │  │      │  └─interceptor
│  │  │  │      │          UserInterceptor.java
│  │  │  │      │
│  │  │  │      ├─pojo  // 各个文件对应本身的业务层，业务层调用Dao层来实现与数据库的交互
│  │  │  │      │  │  Actions.java
│  │  │  │      │  │  Users.java
│  │  │  │      │  │
│  │  │  │      │  ├─bo
│  │  │  │      │  │      ActionCommentBO.java
│  │  │  │      │  │      ActionPrisedBO.java
│  │  │  │      │  │      WXSessionBO.java
│  │  │  │      │  │
│  │  │  │      │  └─vo
│  │  │  │      │          ActionsVO.java
│  │  │  │      │
│  │  │  │      ├─service //各个文件对应本身的控制层，被控制层调用
│  │  │  │      │  │  ActionsService.java
│  │  │  │      │  │  UsersService.java
│  │  │  │      │  │
│  │  │  │      │  └─impl
│  │  │  │      │          ActionsServiceImpl.java
│  │  │  │      │          UsersServiceImpl.java
│  │  │  │      │
│  │  │  │      └─utils //工具类
│  │  │  │              DateUtil.java //日期工具类
│  │  │  │              FaceConfig.java // 
│  │  │  │              HttpClientUtil.java // 客户端的工具类 专门用于发送http请求
│  │  │  │              JqGridResult.java //返回jqGrid的数据格式
│  │  │  │              JsonUtils.java // 自定义响应结构, 转换类,对象、list - 字符串
│  │  │  │              MyMapper.java //继承自己的MyMapper
│  │  │  │              WXConfig.java //设置微信小程序appid与secre
│  │  │  │              XIAOJSONResult.java //自定义响应数据结构
│  │  │  │

│  │  │
│  │  └─resources
│  │      │  application.yml  //与本地数据库相连接的配置信息
│  │      │  file.properties
│  │      │



**Gdesign-qian 前端结构目录**

│  .eslintrc.js
│  app.js  //微信小程序入口
│  app.json //配置文件路径，配置窗口的表现，配置tab标签
│  app.wxss // 页面CSS
│  project.config.json //项目配置文件，小程序名称，appid,用于保存开发者自定义的配置信息
│  project.private.config.json
│  sitemap.json
│
│          test.wxss
│
├─images //图片加载库
│      add.png
│      camera.png
│      circle_no.png
│      circle_yes.png
│      close.png
│      comment-blue.png
│      comment.png
│      contact-active.png
│      contact.png
│      face.png
│      home-active.png
│      home.png
│      link-01.png
│      link-02.png
│      message-active.png
│      message.png
│      me_no.png
│      me_yes.png
│      prize-blue.png
│      prize.png
│      prize_yes.png
│      share.png
│      timeline1.jpg
│
├─pages
│  ├─anwser //用于展示面试题目功能中题目的答案
│  │      anwser.js
│  │      anwser.json
│  │      anwser.wxml
│  │      anwser.wxss
│  │
│  ├─caculate //用于计算题目的点击数
│  │      caculate.js
│  │      caculate.json
│  │      caculate.wxml
│  │      caculate.wxss
│  │
│  ├─companyemploy //招聘岗位的详细信息
│  │      companyemploy.js
│  │      companyemploy.json
│  │      companyemploy.wxml
│  │      companyemploy.wxss
│  │
│  ├─companylist //招聘公司的列表
│  │      companylist.js
│  │      companylist.json
│  │      companylist.wxml
│  │      companylist.wxss
│  │
│  │
│  ├─detail //用户发帖的详情
│  │      detail.js
│  │      detail.json
│  │      detail.wxml
│  │      detail.wxss
│  │
│  ├─home //小程序主界面，有轮播图功能，以及项目主要功能的导航栏
│  │      home.js
│  │      home.json
│  │      home.wxml
│  │      home.wxss
│  │
│  ├─index //用于获取微信用户信息
│  │      index.js
│  │      index.json
│  │      index.wxml
│  │      index.wxss
│  │
│  ├─indextwo //获取所有用户的帖子
│  │      indextwo.js
│  │      indextwo.json
│  │      indextwo.wxml
│  │      indextwo.wxss
│  │
│  │
│  ├─information //用于获取新闻，资讯的详情信息
│  │      information.js
│  │      information.json
│  │      information.wxml
│  │      information.wxss
│  │
│  ├─kefu //在线客服功能，调用的是微信官方API
│  │      kefu.js
│  │      kefu.json
│  │      kefu.wxml
│  │      kefu.wxss
│  │
│  ├─logs
│  │      logs.js
│  │      logs.json
│  │      logs.wxml
│  │      logs.wxss
│  │
│  ├─me //展示用户自己的帖子详情
│  │      me.js
│  │      me.json
│  │      me.wxml
│  │      me.wxss
│  │
│  │
│  ├─publish //用户上传视频，图片
│  │      publish.js
│  │      publish.json
│  │      publish.wxml
│  │      publish.wxss
│  │
│  ├─titilelist //面试题目分类列表
│  │      titlelist.js
│  │      titlelist.json
│  │      titlelist.wxml
│  │      titlelist.wxss
│  │
│  ├─userinfo //用户登录，退出
│  │      userinfo.js
│  │      userinfo.json
│  │      userinfo.wxml
│  │      userinfo.wxss
│  │
│  └─wode //发布帖子功能
│          wode.js
│          wode.json
│          wode.wxml
│          wode.wxss
│
└─utils
        cos-wx-sdk-v5.js
        tools.wxs
        util.js





