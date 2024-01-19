---
layout: project
type: project
image: img/testharness/testharness-square.png
title: "Test Harness"
date: 2023
published: true
labels:
  - Scripted Test Harness
summary: "Me and a classmate developed an automatic script to test website functionality."
---

<div class="text-center p-4">
  <img width="500px" src="../img/MouseShop/landing.png" class="img-thumbnail" >
</div>

Micromouse is an event where small robot “mice” solve a 16 x 16 maze.  Events are held worldwide.  The maze is made up of a 16 by 16 gird of cells, each 180 mm square with walls 50 mm high.  The mice are completely autonomous robots that must find their way from a predetermined starting position to the central area of the maze unaided.  The mouse will need to keep track of where it is, discover walls as it explores, map out the maze and detect when it has reached the center.  having reached the center, the mouse will typically perform additional searches of the maze until it has found the most optimal route from the start to the center.  Once the most optimal route has been determined, the mouse will run that route in the shortest possible time.

For this project, I was the lead programmer who was responsible for programming the various capabilities of the mouse.  I started by programming the basics, such as sensor polling and motor actuation using interrupts.  From there, I then programmed the basic PD controls for the motors of the mouse.  The PD control the drive so that the mouse would stay centered while traversing the maze and keep the mouse driving straight.  I also programmed basic algorithms used to solve the maze such as a right wall hugger and a left wall hugger algorithm.  From there I worked on a flood-fill algorithm to help the mouse track where it is in the maze, and to map the route it takes.  We finished with the fastest mouse who finished the maze within our college.

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

You can find out more by visiting the [Test Harness Repo](https://github.com/citycoding/ITM353_S23_repo).
