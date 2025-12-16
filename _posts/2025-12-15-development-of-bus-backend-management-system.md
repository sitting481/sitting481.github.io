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

**Requirements Analysis and Interface Design**: Referenced existing management dashboard styles, adopted a tab-based and card-style layout to ensure the sidebar and top bar are not obscured, and unified year filtering and date selection rules.

**Frontend Implementation**: Used Vue Composition API and ECharts to build chart components, handling rendering timing (v-if, nextTick/setTimeout), responsive sizing, and axis/grid optimization. Element Plus was used for filter forms and paginated tables. Export functionality was implemented using xlsx.

**Backend Implementation**: Wrote aggregate SQL queries in MyBatis, optimized grouping and subqueries for only_full_group_by mode. Unified order status filtering to paid/finished. Added passenger capacity fields and passenger load rate calculations. Removed PDF generation and retained Excel export functionality.

**Testing and Iteration**: Based on feedback, made multiple adjustments to chart sizing, grids, axis scales, and data filtering logic, fixing issues such as no data scenarios, SQL errors, and export exceptions.

## Project Achievements

**Operational Data Dashboard**: Year-over-year comparison of annual average passenger load rates across all routes, route profitability distribution, and hourly (monthly) passenger flow distribution, with support for refresh and year switching.

**Management Features**: Query, pagination, and Excel export for orders, vehicles, drivers, and safety records. Date selection is limited to the range of 2024-2026.

**Data Consistency**: Passenger capacity is calculated based on paid and finished orders, capacity is taken from the rated passenger capacity of route vehicles. Route profitability statistics include paid and completed orders without deduplicating passenger counts.

**User Experience Optimization**: Charts do not obscure navigation, cards adapt to content height, horizontal axis labels display completely, and exports are unified to xlsx format.

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

Through multiple rounds of feedback, I learned the importance of frontend layout details and chart rendering timing. Proper min-height, grid layouts, and delayed rendering can significantly improve visualization performance.

Backend aggregation requires careful grouping in strict SQL mode. Status values and time filtering must align with real data, otherwise "no data" scenarios can easily occur.

Unified status enums, year/date constraints, and export formats can reduce communication overhead between frontend and backend, improving user experience.
