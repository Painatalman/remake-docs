---
layout: layout.hbs
title: A Simple Example App
---

Let's check how easy it is to **create a TODO app in Remake**, where you can create and update items on a TODO list.

## A Simple, Working Todo List App

The code below is all you need to create a **fully-functional TODO app in Remake:**

<div class="line-numbers">
{% raw %}
```html
<div object>
  <ul array key="todos" sortable>
    {{#for todo in todos}}
      <li 
        object 
        key:text="@innerText"
        edit:text
      >{{default todo.text "New todo item"}}</li>
    {{/for}}
  </ul>
  <button new:todo>Add Todo</button>
</div>
```
{% endraw %}
</div>

<img class="image--small image--border" src="/static/todo-app.gif">

This is a real app. You can try it by [installing Remake](/install-and-setup), adding this code to your `app/pages/app-index.hbs` template, and opening `http://localhost:3000`!

Really, this is all you need for a TODO app in Remake. But this app allows for more than just managing items in a list!

### ⭐️ Features of the app
Besides its code simplicity, what makes this TODO app so interesting is that it allows **managing list items per user**.

With this app, each user can:

* sign up for an account to create their own todo list
* add new items to a list
* edit the text of each item
* remove each item in their list
* reorder their todos by dragging them
* share their todo list with a friend

### How is this possible?

This is possible because Remakes takes a different approach from the *status quo*, one that opens up a lot of possibilities!

While most frameworks treat HTML as static, Remake treats HTML as the source of dynamic data, letting you add web app capabilities directly to an HTML template.

<div class="spacer--16"></div>

### How does this code work?

Line by line documentation:

<div class="line-numbers">
{% raw %}
```html
<!-- This element is converted into an object -->
<div object> 
  <!-- This element is converted into an array,
       labeled with "todos", and all the elements
       inside it can be reordered with drag-and-drop
  -->
  <ul array key="todos" sortable>
    <!-- We loop through any existing todos -->
    {{#for todo in todos}}
      <!-- 
        This is an object that has a key called "text"
        and the value of "text" is the innerText of the element.
        The user can edit this element by clicking on it
      -->
      <li 
        object 
        key:text="@innerText"
        edit:text
      >{{default todo.text "New todo item"}}</li>
    {{/for}}
  </ul>
  <!-- This will render a new "todo" item inside the list -->
  <button new:todo>Add Todo</button>
</div>
```
{% endraw %}
</div>





