---
layout: post
title: "Node first browser development"
date: 2018-04-20
categories: musings
tags: [development,javascript,node,angular]
image:
  feature: javascript.jpg
  teaser: javascript-teaser.jpg
  credit:
  creditlink:
---

While building an [open source library recently](), I inadvertently built it in a way that turned out to be a better approach to building browser based Javascript tool. I built it using the [Kent C. Dodds approach]() to open source Javascript libraries, and what I found was that it was much quicker to develop in node than in a browser especially when you throw in test driven development.

The long and short of it is this: building your application in node with tests makes your browser based application better and more maintainable.

With modern frameworks and their data bindings, **the rendered view should be no more than a pretty representation of the model and a way for the user to update the model**. Effectively if you put a 1 second interval around your endpoint call to save data, it should always have the correct data ready to be sent.

**All actions on the page should be accessible programmatically.** The view is just the interface for the user to manage the model.

So if all actions should be accessible programmatically, then it makes sense to build your library in node first. It makes it easier to test and quicker to develop because you can have your tests in a terminal with a watch on it so you can see immediately if your code is doing what it's supposed to. That and verify that your new changes didn't break any existing features.

This is an extension of the idea of [separating your logic from your framework]() in that you have as minimal dependencies on your application as possible.

Example:

```html
<button ng-click="$ctrl.showStatus = !$ctrl.showStatus">Toggle status</button>
```

**Don't do this!** Logic in the controller limits testability.

Here's a better way:

```html
<button ng-click="$ctrl.toggleStatus()">Toggle status</button>
```
```javascript
class MyPage {
    toggleStatus() {
        this.showStatus = !this.showStatus;
    }
}
```

You may think this is nitpicky but it makes the code more testable and adheres to the principle of the view being the visual layer and not the logic layer. You can't test the expression in the ng-click in the first example but you can in the second. Node first development forces you to write it in the form of the second because there is no html in Node!

**Node first development yields a more testable codebase.**

With the latter you can now run a test that says:

```javascript

// set showStatus to false
// expect it to be false
// run toggleStatus()
// expect showStatus to be true
```

You can't do this with the former.

Here's how to do it.
* kent c. dodds tutorial on egghead
* UMD

