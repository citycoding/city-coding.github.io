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
  <img width="700px" src="../img/toaster_eats.png" class="img-thumbnail" >
</div>

### Project Overview
This project was a collaboration between me and my classmates in ICS 314 to create a website called Toaster Eats. The goal of this project was to create a functional and practical web application for UH students to share recipes. Users are able to add recipes, search for recipes, find ingredients, and find stores for the ingredients. The project spanned a little over a month and took a collaborative effort from Toaster Eats group members to produce a fully functional website.

### Contribution & Experience
I had many learning opportunities with this project and played a very active role in developing the website. Some of my key contributions are creating our logo, creating the initial navigation bar, deploying to Digital Ocean, enabling HTTPS, adding a favicon, creating and setting up a custom domain name, and adding all continuous integration availability tests. 


Here is some code that illustrates how continuous integration availability tests were implemented:

```cpp

test('Test: Recipes Page is Displayed', async (testController) => {
  await navBar.gotoSignInPage(testController);
  await signinPage.signin(testController, credentials.username, credentials.password);
  await navBar.gotoRecipesPage(testController);
  await recipesPage.isDisplayed(testController);
});

test('Test: Add Recipes Page is Displayed', async (testController) => {
  await navBar.gotoSignInPage(testController);
  await signinPage.signin(testController, credentials.username, credentials.password);
  await navBar.gotoAddRecipesPage(testController);
  await addRecipesPage.isDisplayed(testController);
});

```

You can find out more by visiting the [Toaster Eats Organization](https://github.com/Toaster-Eats).
