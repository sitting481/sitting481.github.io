---
layout: post
title: WeChat Mini Program Development
author: Siting Chen
date: 2025-03-01 23:18 +0800
last_modified_at: 2025-05-20 09:08:25 +0800
tags: [self-service ordering, miniprogram]
---

This is a WeChat Mini Program project for online self-service ordering.

## Table of Contents

- [Project Description and Goal](#Project Description and Goal)
- [Learning and execution process](#Learning and execution process)
- [Project Achievements](#Project Achievements)
- [Personal reflection](#Personal reflection)


## Project Description and Goal

This project is an online self-service ordering system based on a WeChat Mini Program, designed to provide a convenient digital ordering solution for the food and beverage industry. Through the WeChat Mini Program platform, users can complete the entire ordering process, including browsing menus, selecting items, placing orders and making payments, requesting refunds, and contacting the restaurant.

## Learning and execution process

As a beginner, I decided to take on the challenge of building a complete WeChat Mini Program e-commerce project. Initially, I knew nothing about WeChat Mini Program development and had no idea what features a fully functional mini-program should include. Therefore, I referred to numerous online ordering mini-programs to study their design styles, button layouts, and functional designs. After examining a wide range of online ordering mini-programs, I gained inspiration and began designing my own online ordering WeChat Mini Program.

Phase 1: I started by creating a new mini-program project in the WeChat Developer Tools and selected the TypeScript template. At first, I was confused by the .wxml, .wxss, and .js files and didn’t understand their respective roles. By referring to the official documentation, I gradually grasped the four core components of mini-programs: WXML for structure, WXSS for styling, JS for logic, and JSON for configuration.

Phase 2: Frontend Page Development
I decided to start with the simplest page—the homepage. Initially, I could only write basic text and buttons, but later I learned to use the scroll-view component to implement scrolling effects. When I needed more complex UI components, I discovered the lin-ui component library, which significantly improved my development efficiency. I learned how to integrate third-party component libraries into the mini-program and gradually built functional modules such as user information display and product recommendations.

Phase 3: Backend Service Setup
After making progress on the frontend, I realized the need for a backend to provide data support. I chose Node.js + Express as the backend technology stack because JavaScript allowed me to reuse my frontend knowledge. I learned how to design RESTful APIs, use Express’s routing system, and connect to a MySQL database.

Phase 4: Frontend-Backend Integration
This was the most challenging phase. I learned how to use wx.request in the mini-program to send HTTP requests, handle asynchronous data loading, and display backend data on the frontend.

Phase 5: Feature Enhancement and Optimization
As the project progressed, I added more features: product lists, detail pages, shopping cart, user center, and more.

## Project Achievements

The project developed multiple core pages, including functional modules such as user authentication, product display, shopping cart management, and personal center. In terms of feature implementation, I built a complete e-commerce business workflow: users can log in via WeChat authorization, browse product lists and details, add desired items to the shopping cart, submit orders, and manage personal information.



![主页](<table style="width: 100%; border-collapse: collapse; margin: 20px 0;">
<tr>
<td style="width: 33.33%; text-align: center; padding: 10px; vertical-align: top;">
<img src="/images/wechat-home.jpg" alt="微信小程序主页界面" style="width: 100%; max-width: 300px; height: auto; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.1);">
<p style="margin-top: 8px; font-size: 14px; color: #666;">微信小程序主页界面</p>
</td>
<td style="width: 33.33%; text-align: center; padding: 10px; vertical-align: top;">
<img src="/images/wechat-menu.jpg" alt="微信小程序菜单页面" style="width: 100%; max-width: 300px; height: auto; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.1);">
<p style="margin-top: 8px; font-size: 14px; color: #666;">微信小程序菜单页面</p>
</td>
<td style="width: 33.33%; text-align: center; padding: 10px; vertical-align: top;">
<img src="/images/wechat-order.jpg" alt="微信小程序订单页面" style="width: 100%; max-width: 300px; height: auto; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.1);">
<p style="margin-top: 8px; font-size: 14px; color: #666;">微信小程序订单页面</p>
</td>
</tr>
</table>)



![菜单页](<table style="width: 100%; border-collapse: collapse; margin: 20px 0;">
<tr>
<td style="width: 33.33%; text-align: center; padding: 10px; vertical-align: top;">
<img src="/images/wechat-home.jpg" alt="微信小程序主页界面" style="width: 100%; max-width: 300px; height: auto; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.1);">
<p style="margin-top: 8px; font-size: 14px; color: #666;">微信小程序主页界面</p>
</td>
<td style="width: 33.33%; text-align: center; padding: 10px; vertical-align: top;">
<img src="/images/wechat-menu.jpg" alt="微信小程序菜单页面" style="width: 100%; max-width: 300px; height: auto; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.1);">
<p style="margin-top: 8px; font-size: 14px; color: #666;">微信小程序菜单页面</p>
</td>
<td style="width: 33.33%; text-align: center; padding: 10px; vertical-align: top;">
<img src="/images/wechat-order.jpg" alt="微信小程序订单页面" style="width: 100%; max-width: 300px; height: auto; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.1);">
<p style="margin-top: 8px; font-size: 14px; color: #666;">微信小程序订单页面</p>
</td>
</tr>
</table>)



## Personal reflection

Throughout this course project, I have learned various concepts and techniques related to full-stack development, including front-end design, back-end architecture, database management, and API integration. I also gained a comprehensive understanding of e-commerce systems and the challenges involved in building scalable web applications. This project helped me develop my full-stack development skills and prepared me to tackle real-world development challenges.
