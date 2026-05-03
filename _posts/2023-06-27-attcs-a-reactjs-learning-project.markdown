---
layout: post
title:  "ShaGanPyo - An Automatic Timetable Creator"
date:   2023-06-27 09:00:00 +0900
category: project
mathjax: true
image: /assets/images/shaganpyo/shaganpyo.png
---

<img src="/assets/images/shaganpyo/shaganpyo.png" title="ShaGanPyo"/>
 
**Translation -** *Get the Timetable You Want, Automatically, with ShaGanPyo.*
*The Automatic Timetable Creator Program for SNU Students, ShaGanPyo.*

<div class="gap"></div>

**ShaGanPyo**(**샤간표** in Korean) is a React-based web application designed to help Seoul National University (SNU) students manage their class schedules and generate optimized timetables through an automated generation feature.

<div class="gap"></div>

The name, **ShaGanPyo**, is a portmanteau of "Sha"—the nickname SNU students use for the university’s iconic main gate—and "Si Gan Pyo," the Korean word for "timetable."

# The Goal

SNU students must consider numerous factors when registering for courses before each semester. Because students cannot take two courses with overlapping lecture times, schedule planning becomes extremely complicated—especially for those with heavy course loads. Additionally, due to the large size of the SNU campus, students must account for walking time between buildings. Many also prefer to avoid morning classes or excessively long back-to-back schedules.

<div class="gap"></div>

**ShaGanPyo** simplifies this process. **ShaGanPyo** allows students to easily add multiple sections of the same subject into a cart and automatically generates an ideal timetable based on their preferences with a single click of the ‘Auto Generate’ button.



# Key Features
## Manual Timetable Creation

The **Search Courses** page serves as the primary interface of ShaGanPyo, where students can manually build their schedules. By typing a course name into the search bar, you can find and add it to the timetable on the right. The search function also features ‘search by abbreviation,’ enabling students to find courses quickly. 

<div class="gap"></div>

**Example:** Instead of typing "Computer Architecture," a student can simply type "Comp Arch" to find the relevant listings immediately.

{% include video.html src="/assets/videos/shaganpyo/timetable.mp4" caption="Manual Timetable Creation Demo" %}

The first page is for exploring courses and provides a testground for trying out several schedules, creating them by hand before auto-generating timetables.


## Automatic Timetable Generation

The core strength of ShaGanPyo lies in the **Add Courses** and **Generate Timetable** pages. This workflow is designed for automated scheduling.

<div class="gap"></div>

On the **Add Courses** page, you can search for a subject (by its full name or abbreviation) to see all available sections. You can then select and add specific sections to your list. Since some courses share a subject name but are restricted to certain majors, this feature helps students avoid adding classes they are ineligible for or do not prefer.

{% include video.html src="/assets/videos/shaganpyo/autocreate.mp4" caption="Automatic Timetable Generation Demo" %}

On the **Generate Timetable** page, clicking the large "Generate" button prompts ShaGanPyo to process every possible combination of your selected courses. The system automatically filters out any schedules where two or more courses have overlapping lecture times, presenting a curated selection of valid timetables to the student. The first result displayed (Timetable #1) represents the most highly recommended option. To ensure the results align with their specific needs, students can customize the prioritization rules used to rank and filter these generated timetables at the **Settings** page.


## Custom Schedules

ShaGanPyo recognizes that a student's life extends beyond the classroom. With the **Custom Schedules** feature, students can add personal commitments—such as group studies, internships, or club activities—and force the system to account for these blocks when automatically generating the final timetable.

{% include video.html src="/assets/videos/shaganpyo/custom.mp4" caption="Custom Schedule Demo" %}


# Development Timeline
This was both a toy project and a learning project. The development of ShaGanPyo started shortly after I started learning ReactJS.

* **Feb 2023** -- Started developing with ReactJS
* **Mar 2023** -- Created the search & timetable features
* **Apr 2023** -- Added the timetable auto-generation feature, Recoded to TypeScript
* **May 2023** -- Added timetable prioritization, Added mobile UI
* **Aug 2023** -- Released version 1.0 <br> *First introduced to SNU students and was actually used during course registration of the fall semester*
* **Jan 2024** -- Started the recoding of the entire project to use React Redux
* **Jul 2024** -- Finished recoding to React Redux
* **Jan 2026** -- Optimization and design improvements
* **Feb 2026** -- Added English support

# Check Out ShaGanPyo

You can try out ShaGanPyo using [this link][shaganpyo-site]{:target="_blank"}. The website is hosted with Firebase.

[shaganpyo-site]: https://shaganpyo.web.app/