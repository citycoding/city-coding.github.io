---
layout: project
type: project
image: img/toaster-eats/toaster_square.png
title: "Toaster Eats"
date: 2024
published: true
labels:
  - Final Project
  - Web Design
  - Software Engineering
summary: "My team (Toaster Eats) developed a website that allows UH students to create and share recipes while supporting local businesses."
---

<div class="text-center p-4">
  <img width="500px" src="../img/toaster_eats.png" class="img-thumbnail" >
</div>

This project was a collaboration between me and my classmates in ICS 314 to create a website called Toaster Eats. The goal of this project was to create a functional and practical web application for UH students to share recipes. Users are able to add recipies, search for recipies, find ingredients, and find stores for the ingredients. The project spanned a little over a month and took a collaborative effort from Toaster Eats group members to produce a fully functional website.

The establishment of automatic testing eliminates the need for individual test cases on each page. Instead a standardized test can be created to test functionality. This saves precious time that can be spent on further capability expansion and project development. I learned how this can optimize the allocation of resources when working on time sensitive projects.


Here is some code that illustrates how automatic script functionality was used:

```cpp
function test(func, name, properties)
    {
        var test_name = name ? name : next_default_name();
        properties = properties ? properties : {};
        var test_obj = new Test(test_name, properties);
        test_obj.step(func);
        if (test_obj.status === test_obj.NOTRUN) {
            test_obj.done();
        }
    }

    function async_test(func, name, properties)
    {
        if (typeof func !== "function") {
            properties = name;
            name = func;
            func = null;
        }
        var test_name = name ? name : next_default_name();
        properties = properties ? properties : {};
        var test_obj = new Test(test_name, properties);
        if (func) {
            test_obj.step(func, test_obj, test_obj);
        }
        return test_obj;
    }

    function setup(func_or_properties, maybe_properties)
    {
        var func = null;
        var properties = {};
        if (arguments.length === 2) {
            func = func_or_properties;
            properties = maybe_properties;
        } else if (func_or_properties instanceof Function){
            func = func_or_properties;
        } else {
            properties = func_or_properties;
        }
        tests.setup(func, properties);
        output.setup(properties);
    }

```

You can find out more by visiting the [Toaster Eats Organization](https://github.com/Toaster-Eats).
