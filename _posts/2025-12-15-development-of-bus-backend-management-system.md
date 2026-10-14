---
layout: post
title: Bus Operations Management & Analytics System
author: ChenSiting
date: 2025-09-01 09:00 +0800
last_modified_at: 2026-04-15 09:08:25 +0800
tags: [bus management, data analysis, data visualization, full-stack]
---


## Table of Contents

- [Project-Description-and-Goal](#project-description-and-goal)
- [Learning-and-Execution-Process](#learning-and-execution-process)
- [Project-Achievements](#project-achievements)
- [Personal-Reflection](#personal-reflection)

## Project Description and Goal

This is a bus operations management and analytics system with a separated front-end/back-end architecture. The front end is built with Vue 3, Element Plus, and ECharts, while the back end uses Spring Boot, MyBatis, and MySQL. It covers route management, trip scheduling, vehicle tracking, driver management, order processing, and operational statistics.

The system integrates route, trip, vehicle, driver, and order data into a unified operational dataset and provides interactive data visualization, order and vehicle management, and Excel report export. Its dashboards include annual average passenger load rates by route, route revenue distribution and profitability analysis, and monthly passenger flow distribution, supporting dispatch decision-making and daily operational efficiency.

## Learning and Execution Process

After completing my internship at Foshan Automobile Transport Group Co., Ltd., I gained a clear understanding of real business requirements and system design logic in bus operations. Inspired by this experience, I independently designed and developed this system to address practical pain points in operational data management and decision-making. I referred to architectural approaches from open-source management systems and advanced the project in four stages.

Stage 1: Frontend Development and Data Visualization

I focused on user interaction and data visualization. I implemented online route inquiry and map display, enabling dynamic visualization of routes, stops, and schedules. I also built an operational statistics dashboard with three core visualizations: a trend line chart comparing annual average passenger load rates across routes, a pie chart analyzing revenue distribution by route, and a line chart showing monthly aggregated passenger flow. The system also provides a comprehensive business management interface and flexible report export, improving operational efficiency and data accessibility.

Stage 2: Back-End Service and Data Analysis

Using Spring Boot, I built a complete back-end service system with management interfaces for core business modules such as routes, schedules, vehicles, drivers, and orders. The back end also supports operational statistics and report generation. Through SQL aggregation queries, it dynamically calculates key metrics, including annual average passenger load rate by route, revenue distribution by route, and monthly passenger flow. All list interfaces use back-end pagination to ensure query performance and response efficiency for large datasets.

Stage 3: System Testing and Validation

I conducted comprehensive interface and functional testing, covering CRUD operations for routes, schedules, vehicles, drivers, and orders; three types of operational statistics interfaces; and custom report generation and Excel export. I also performed functional and compatibility testing on front-end interaction flows and visualization components to ensure system stability and reliability.

Stage 4: Deployment and Launch

I packaged the front-end static resources and back-end Java application separately and deployed them to a local server environment. By configuring domain name resolution, SSL certificates, and system monitoring services, I completed the official release and online deployment, achieving a full development-to-deployment lifecycle.

## Project Achievements

This project delivered multiple core pages and functions for bus operation inquiry, management, and statistics. These include:

· A route map query system that displays routes, stations, and schedules.
· Filterable and paginated management interfaces for orders, vehicles, drivers, and safety records, with Excel export capabilities.
· A custom report generator that produces and exports reports based on specified conditions.
· An operational data dashboard with three key visualizations: annual average passenger load rate comparisons across routes, route revenue · distribution, and monthly passenger flow distribution.

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

Through this project, I achieved substantial progress in full-stack development and data analytics. On the front end, I learned how to transform business data into interactive visualizations and used ECharts to build professional data dashboards. I addressed challenges such as rendering sequence control, responsive design, and detailed axis configuration, ensuring clear and professional data presentation. On the back end, I strengthened my ability to write complex SQL aggregation queries and design statistical metric models based on business logic. I also established standardized API specifications and a robust data export framework, improving the rigor of the system architecture. This experience not only consolidated my technical skills but also improved my ability to manage the transition from business requirements to technical implementation, laying a solid foundation for future work in data analysis and system design.
