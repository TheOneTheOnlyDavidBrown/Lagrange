---
layout: post
title: "Composition v. Inheritance"
date: 2017-04-29
categories: musings
tags: [open-source,git,github,advice]
comments: true
image:
  feature: computer.jpg
  teaser: computer-teaser.jpg
  credit:
  creditlink:
---

Designing software like a database
Preface
I'm not saying inheritence is bad, just that it shouldn't be abused.
I know JavaScript classes aren't real classes

One thing is constant in all of software development - your project requirements will change. In order mitigate the cost of change, you need a good pattern. Inheritence can work but it isn't always the best pattern to use. Every developer at some point has been told "don't repeat yourself" or DRY. This is true but it lends itself to refactoring into poor designs. Poor design decisions cost your company money, can delay a product launch, and usually end with the product being less than stellar and difficult to maintain.

By using a software pattern than is flexable, you will reduce the cost of change, make the project more maintainable, and most likely finish the project earlier. There are a plethora of design patterns but I want to focus on the composition design pattern and how it can be used in place of inheritance. This is not a one size fits all pattern and should only be used where it make sense. As should inheritence.

If you're familiar with Entity Relationship Diagrams (ERDs), you'll realize that database design does not have inheritence but rather a 'has' relationship. A person has many shoes, for example. You will also realize that a properly thought out database is very flexable and prevents a lot of anomolies. So when you develop software, you should put yourself into a database architect mindset and develop with a pattern that mimicks a database design.

For sake of argument, let's say you're developing a game. You have two classes of characters named Mario and Bowser. You realize both of them share common methods of `jump` and `move` so you do the logical thing and refactor that into a parent class called `character` and inherit it in your classes, right? Sure at this point in time it makes sense but it's not an ideal pattern because it's about this time that your boss comes to and says 'we are adding a new character...a ghost.' And you think "hmmm a ghost doesn't have the same physics as the other two chararcters but it's sort of like it" At this point you have the decision to make. Do I inherit the character class because a ghost is "sort of like" it? No! this is the pitfall of inheritance. So what is a good pattern in this case? Composition. Let's now take the `jump` and `move` methods and move them into a Physics class.

Composition vs Inheritance

The child-parent relationship in inheritance is an `is a` relationship. Where as composition, much like a database, has an `has a` relationship. This gives us a lot of advantages right off the bat. It has better encapsulation so you can edit the physics class, it makes the parent class smaller, and you can have multiple physics attributes so if the character is in an environment where he can't jump as high you can swap out the physics and swap the original back.

* encapsulation
* reuse
* swappable





inherit
* ripple effect








intro (ie think like youre designing a database)
what is composition?
benefits
what is inheritance?
what problem does it solve?
when to use
