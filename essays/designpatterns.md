---
layout: essay
type: essay
title: "The Time and Place to use Design Patterns"
# All dates must be YYYY-MM-DD format!
date: 2024-12-03
published: true
labels:
  - Design
  - Style
  - UI
---

<img width="300px" style="padding: 5px" class="rounded float-start" src="../img/DesignEssayImage.png" alt="Factory Creating Restaurants">

## Designs

<p>Design patterns are reusable solutions to common problems in software design, helping make coding more efficient. In software engineering, design patterns reduce the amount of hardcoding required, making it easier to scale and maintain projects. As I've been working on the final project for ICS 314, I've come to realize just how important design patterns are. For example, our final project involves creating an app that lists all the restaurants at UH Manoa. By using a "Restaurant" model, we can easily implement various features, such as displaying restaurant cards, pinning locations on a Google Map, and adding images.</p>
<p>Without design patterns, managing a large-scale project would be a nightmare. This became clear when I attempted to recreate SoundCloud using React. I manually entered every image, title, author, and link for each sound. Instead of this tedious approach, I could have used a Factory pattern to generate the individual cards for each trending sound, streamlining the process.</p>
<img style="padding: 5px" class="rounded float-start" src="../img/SoundCloudRecreate.png" alt="My React SoundCloud recreation">

## Types Of Design and When to Use Them

### Factory

<p>The Factory Design Pattern serves the role of a "factory" by creating multiple instances of a class as needed. For instance, in our project, instead of manually entering each restaurant, we could use a factory to generate multiple restaurant card components based on the data we have in our database. This simplifies the process, allowing for easy scalability and maintaining clean, reusable code. </p>

### Singleton

<p>The Singleton Design Pattern ensures that a class has only one instance and provides a global point of access to that instance. This pattern is useful when you need to control access to shared resources, such as a configuration object or a database connection. In our project, for example, we could use the Singleton pattern to manage user session data, ensuring that only one instance of the session object exists throughout the app.</p>

### Observer

<p>The Observer Design Pattern is used when a change in one object needs to be reflected in another without tightly coupling the objects. For example, if a user makes a change to a restaurant's details, the observer pattern could be used to update the restaurant's details in real-time across all views of the app (e.g., updating the list of restaurants shown or the map markers without needing to reload the page).</p>

### MVC

<p>The MVC Design Pattern divides an application into three interconnected components: the Model (the data), the View (the UI), and the Controller (which manages user input and updates the model). This separation of concerns allows for better organization and maintainability. In our project, the Model would represent the restaurant data, the View would display the list of restaurants, and the Controller would manage the interaction between the user and the data (e.g., filtering restaurants based on the user's preferences).</p>


