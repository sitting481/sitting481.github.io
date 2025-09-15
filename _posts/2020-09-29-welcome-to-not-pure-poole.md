---
layout: post
title: WeChat Mini Program Development
author: Siting Chen
date: 2025-03-01 23:18 +0800
last_modified_at: 2025-05-20 09:08:25 +0800
tags: [self-service ordering, miniprogram]
---

This is a WeChat Mini Program project for online self-service ordering.

## 目录

- [项目概述](#Project description and goal)
- [学习和执行过程](#Learning and execution process)
- [项目成就](#Project Achievements)
- [个人反思](#Personal reflection)


## Project description and goal

This project is an online self-service ordering system based on a WeChat Mini Program, designed to provide a convenient digital ordering solution for the food and beverage industry. Through the WeChat Mini Program platform, users can complete the entire ordering process, including browsing menus, selecting items, placing orders and making payments, requesting refunds, and contacting the restaurant.

## Learning and execution process

作为一个初学者，我决定挑战一个完整的微信小程序电商项目。刚开始时，我对微信小程序开发一无所知，也不知道一个能正式应用的微信小程序应该要包括什么功能。因此我参考了大量的线上点单的微信小程序，学习别人的样式设计，按键排布，功能设计。在我查看了大量的线上点单的小程序后，得到了启发，并着手设计自己的线上点餐微信小程序。
第一阶段：我首先在微信开发者工具中创建了一个新的小程序项目，选择了TypeScript模板。刚开始看到那些.wxml、.wxss、.js文件时，我感到很困惑，不知道它们各自的作用。通过查阅官方文档，我逐渐理解了小程序的四件套：WXML负责结构、WXSS负责样式、JS负责逻辑、JSON负责配置。

第二阶段：前端页面开发我决定从最简单的首页开始。最初我只会写一些基础的文本和按钮，后来学会了使用scroll-view组件来实现滚动效果。当我需要更复杂的UI组件时，我发现了lin-ui组件库，这大大提高了我的开发效率。我学会了如何在小程序中集成第三方组件库，并逐步构建了用户信息展示、商品推荐等功能模块。

第三阶段：后端服务搭建前端开发到一定程度后，我意识到需要后端来提供数据支持。我选择了Node.js + Express作为后端技术栈，因为JavaScript语言可以让我复用前端的知识。我学会了如何设计RESTful API，如何使用Express的路由系统，以及如何连接MySQL数据库。刚开始写SQL语句时经常出错，但通过不断练习，我逐渐掌握了数据库的基本操作。

第四阶段：前后端联调这是最困难的阶段。我学会了如何在小程序中使用wx.request发送HTTP请求，如何处理异步数据加载，以及如何在前端展示后端返回的数据。

第五阶段：功能完善与优化随着项目的深入，我添加了更多功能：商品列表、详情页、购物车、用户中心等。
我学会了使用小程序的页面跳转、数据传递、本地存储等技术。同时，我也学会了如何优化代码结构，如何提高用户体验，以及如何处理各种异常情况。
收获与成长通过这个项目，我不仅掌握了微信小程序开发的核心技术，还学会了全栈开发的思维模式。我明白了前后端分离的重要性，
学会了如何设计合理的API接口，以及如何构建可维护的代码架构。虽然过程中遇到了很多困难，但每一次解决问题都让我更加自信，也让我对编程有了更深的理解。

## Project Achievements

该项目开发了多个核心页面，包括用户认证、商品展示、购物车管理、个人中心等功能模块。同时，在功能实现方面，我构建了完整的电商业务流程：用户可以通过微信授权登录，浏览商品列表和详情，将心仪商品加入购物车，提交订单和管理个人信息。


## Personal reflection


通过这个项目，我深入学习了微信小程序开发技术，掌握了前后端分离的开发模式，提升了项目管理和团队协作能力。未来将继续优化系统功能，探索更多创新特性。

![测试图片](https://via.placeholder.com/800x400/4CAF50/FFFFFF?text=WeChat+Mini+Program+Screenshot)
