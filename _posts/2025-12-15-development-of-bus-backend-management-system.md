---
layout: post
title: Development of Bus Backend Management System
author: Siting Chen
date: 2025-09-01 09:00 +0800
last_modified_at: 2025-12-15 09:08:25 +0800
tags: [bus management, full-stack, backend, frontend]
---

This is a front-end and back-end separated bus operation management system application covering businesses such as routes, trips, vehicles, drivers, and orders.

## Table of Contents

- [Project-Description-and-Goal](#project-description-and-goal)
- [Learning-and-Execution-Process](#learning-and-execution-process)
- [Project-Achievements](#project-achievements)
- [Personal-Reflection](#personal-reflection)

## Project Description and Goal

This is a bus operation management system built with Vue3 + Element Plus + ECharts on the frontend and Spring Boot + MyBatis + MySQL on the backend, covering route management, trip scheduling, vehicle tracking, driver management, order processing, and operational statistics.

The system provides operational data visualization (including annual average passenger load rates by route, route profitability, and hourly passenger flow distribution), order and vehicle management, and report export functionality (Excel), aiming to improve dispatch decision-making and daily operational efficiency.

## Learning and Execution Process

Upon completing my internship at Foshan Automobile Transport Group Co., Ltd., I gained a deep understanding of the functional requirements and system design logic in actual enterprise operations. Inspired by this experience, I decided to independently design and develop a backend management system tailored to real business scenarios to address potential pain points in daily enterprise operations. During the system design process, I referenced architectural approaches from various excellent management systems on open-source platforms and progressively advanced the project implementation.

Stage 1: Frontend Development
I focused on user interaction and data visualization, primarily implementing an online route inquiry and map display feature that enables the dynamic visualization of routes, stops, and real-time schedules. Additionally, I built an operational statistics dashboard integrating three core data visualizations: a trend line chart comparing the annual average passenger load rates across all routes by year, a pie chart analyzing revenue distribution by route, and a line chart showing monthly aggregated passenger flow distribution. The system also provides a comprehensive business management interface and flexible report export functionality, significantly enhancing operational efficiency and data portability.

Stage 2: Backend Service Development
Leveraging the Spring Boot framework, I constructed a complete backend service system that offers management interfaces for core business modules such as routes, schedules, vehicles, drivers, and orders. The backend also supports operational statistics and report generation functionalities. Through aggregated queries, it dynamically calculates key metrics, including the annual average passenger load rate per route, revenue distribution by route, and monthly passenger flow distribution. All data list interfaces utilize backend pagination to ensure query performance and response efficiency when handling large datasets.

Stage 3: System Testing and Validation
I conducted comprehensive interface and functional testing, covering CRUD operations for business entities (routes, schedules, vehicles, drivers, and orders), the three types of operational statistics interfaces (annual average passenger load rate, revenue distribution by route, and monthly passenger flow distribution), as well as custom report generation and Excel export functionalities. Additionally, I performed thorough functional and compatibility testing on frontend interaction flows and visualization components to ensure system stability and reliability.

Stage 4: Deployment and Launch
I packaged the frontend static resources and backend Java application separately and deployed them to a local server environment. By configuring domain name resolution, SSL certificates, and system monitoring services, I successfully completed the official release and online deployment of the system, achieving a full-cycle closure from development to launch.

## Project Achievements

This project developed multiple core pages, with functionalities covering bus operation inquiry, management, and statistics. These include: a route map query system that displays lines, stations, and schedules; filterable and paginated management interfaces for orders, vehicles, drivers, and safety records with Excel export capabilities; a custom report generator that produces and exports reports based on specified conditions; and an operational data dashboard offering three key visualizations: annual average passenger load rate comparisons across all lines, line revenue distribution, and monthly passenger flow distribution.

<p style="text-align: center; font-size: 14px; color: #666; margin: 20px 0;">Below are some pages of the project</p>

<table style="width: 100%; border-collapse: collapse; margin: 20px 0;">
<tr>
<td style="width: 50%; text-align: center; padding: 10px; vertical-align: top;">
<img src="/images/bus-line.png" alt="Drawing of Bus Route Map" style="width: 100%; max-width: 400px; height: auto; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.1);">
<p style="margin-top: 8px; font-size: 14px; color: #666;">Drawing of Bus Route Map</p>
</td>
<td style="width: 50%; text-align: center; padding: 10px; vertical-align: top;">
<img src="/images/bus-linecheck.png" alt="Selection of Bus Route Map" style="width: 100%; max-width: 400px; height: auto; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.1);">
<p style="margin-top: 8px; font-size: 14px; color: #666;">Selection of Bus Route Map</p>
</td>
</tr>
</table>

<table style="width: 100%; border-collapse: collapse; margin: 20px 0;">
<tr>
<td style="width: 50%; text-align: center; padding: 10px; vertical-align: top;">
<img src="/images/bus-customize.png" alt="Customize report generation" style="width: 100%; max-width: 400px; height: auto; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.1);">
<p style="margin-top: 8px; font-size: 14px; color: #666;">Customize report generation</p>
</td>
<td style="width: 50%; text-align: center; padding: 10px; vertical-align: top;">
<img src="/images/bus-flowchart-month.png" alt="Monthly Passenger Flow Chart" style="width: 100%; max-width: 400px; height: auto; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.1);">
<p style="margin-top: 8px; font-size: 14px; color: #666;">Monthly Passenger Flow Chart</p>
</td>
</tr>
</table>

<table style="width: 100%; border-collapse: collapse; margin: 20px 0;">
<tr>
<td style="width: 50%; text-align: center; padding: 10px; vertical-align: top;">
<img src="/images/bus-flowchart-year.png" alt="Yearly Passenger Flow Chart" style="width: 100%; max-width: 400px; height: auto; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.1);">
<p style="margin-top: 8px; font-size: 14px; color: #666;">Yearly Passenger Flow Chart</p>
</td>
<td style="width: 50%; text-align: center; padding: 10px; vertical-align: top;">
<img src="/images/bus-piechart.png" alt="Line Benefit Analysis Diagram" style="width: 100%; max-width: 400px; height: auto; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.1);">
<p style="margin-top: 8px; font-size: 14px; color: #666;">Line Benefit Analysis Diagram</p>
</td>
</tr>
</table>

<table style="width: 100%; border-collapse: collapse; margin: 20px 0;">
<tr>
<td style="width: 50%; text-align: center; padding: 10px; vertical-align: top;">
<img src="/images/bus-occupancy.png" alt="Average Passenger Capacity Chart" style="width: 100%; max-width: 400px; height: auto; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.1);">
<p style="margin-top: 8px; font-size: 14px; color: #666;">Average Passenger Capacity Chart</p>
</td>
<td style="width: 50%; text-align: center; padding: 10px; vertical-align: top;">
</td>
</tr>
</table>

## Personal Reflection

Through the comprehensive implementation of this project, I have achieved substantial breakthroughs in full-stack development capabilities. On the frontend side, I mastered the core techniques for transforming business data into interactive visualizations, utilizing ECharts to build professional-grade data dashboards. I delved into resolving critical challenges such as rendering sequence control, cross-device responsive design, and fine-grained axis configuration, ensuring both clarity and professionalism in data presentation. On the backend side, I systematically honed my ability to write complex aggregation queries in SQL, accurately designing statistical metric models based on business logic. Additionally, I established standardized interface specifications and a robust data export framework, thereby enhancing the rigor of the system architecture. This experience has not only solidified my technical skill set but also cultivated my ability to holistically manage the transition from business requirements to technical implementation. It has laid a solid foundation for me to take on more complex responsibilities in system architecture design and product iteration in the future.
