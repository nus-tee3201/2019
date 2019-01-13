{% macro show_main_text() %} 
<div id="main">

### Prior Knowledge: Java and OOP

This module requires you to write Java code almost every week, starting from the very first week. If your Java skills are rusty, do brush up your Java programming skills.

In particular, you may want to **have a look at the new Java 8 features** such as _streams_, _lambdas_, _Optionals_, that may not have been covered in previous Java modules.

CS2103 students: ==This module assumes a reasonable prior knowledge of Java and OOP== because most students taking this module have taken two Java modules before. If you are totally new to Java, you may be better off switching to CS2113 (Software Engineering & Object-Oriented Programming) instead.

### Workload

Given 60% of this module is based on CA, it can appear to be _heavy_. However, **it is not expected that you will spend more time on this module than its peer modules** %%(e.g., if this module is core for you, it should not take more time than other level 2 core modules in your program)%%. 
* Note that the **module contains more things than a typical students can do**, in order to provide enough things for even the strongest students to learn as much as they wish to. 
* This means it is ==**perfectly OK if you don't have time to learn everything the module offers**==. Control your workload based on time you spend for the module in a week e.g., 1-1.5 days per week.
* We have provided a star rating system to guide you when prioritizing which things to do.

<div id="starRatingSystem">

#### Star rating system

<div class="indented">

<p class="lead"> Start with things that are rated one-star and progress to things with more stars. Things rated four stars are optional.
</p>

**Star ratings for Learning Outcomes** (and textbook sections):

* **One-star topics** {{ one_star }}: The topics you need to learn just to keep up with the module. We recommend you to ==learn these topics if you want to pass the module== (i.e. up to a **C** grade).
* **Two-stars topics** {{ two_stars }}: Can get you up to a **B+**.
* **Three-stars topics** {{ three_stars }}: Can get you up to an **A+**.
* **Four-stars topics** {{ four_stars }}: ==Four-star topics are not examinable==. They are for your information only. Omitting them will not affect your grade.

</div>
</div>

</div>
{% endmacro %} 


{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("moduleExpectations", show_main_text) }}
