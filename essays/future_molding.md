---
layout: essay
type: essay
title: "Structural Molding"
# All dates must be YYYY-MM-DD format!
date: 2024-04-25
published: true
labels:

---
<img width="200px" class="rounded float-start pe-4" src="../img/feelingsmart/react_logo.png">

### Shaping Operations
When I started to code a few years ago, I had no concept of how to start a project. I thought there might be a single “right” way to go about coding. I still don’t know if there is an objective “right” way to create a project, but I suspect that the margins between “right” and “mostly right” are very small. These questions tie directly into concepts of design patterns and how they affect project planning, building, and execution. There are many types of design patterns from which to choose. Design patterns often focus on one part of the System Design Life Cycle (SDLC), such as issue testing, implementation, and analysis. Design patterns can also influence the documentation, communication, and coding styles of developers, depending on the design. 

### Decisive Operations
An example of a design pattern used in my Toaster Eats project is the singleton pattern. A singleton design pattern applies to Toaster Eats, in which a single instance can be created and exported to the rest of the application. Our project has a “Recipes” class that manages access to the MongoDB collection named "Recipes." The Recipes instance is created and exported to the application hosted on the server. When users visit the site, they can manipulate the collection data to add new recipes and edit existing recipes. These actions are done through forms, which are the primary way to read and write from the MongoDB database. 

Although I have not coded large-scale applications, I can see the benefits of using a schema to base your designs and operations on. It gives a single function to code around and even serves as a throughput to interact with applications. I believe that design patterns should be used in accordance with the project you are working on, taking into consideration any functionalities and constraints that may be present. It is a core part of architecture to consider when creating and planning a project that may involve multiple users and purposes.
