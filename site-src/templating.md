---
layout: layout.hbs
title: Templating
---

### Handlebars.js

Remake uses [Handlebars.js](https://handlebarsjs.com/) to render every template. All templates are server-rendered.

### Template Variables

These are all the possible template variables you'll have access to in a Handlebars template:

- **Your app's data**
  - On routes preceded by a username, e.g. `/john` or `/john/tasks`, all of the data for that user is loaded into the template and made available
- **globalData**
  - This is static data shared by all templates and all users (loaded from the file `app/data/global-app-data.json`). It's useful for defining global navigation items or page titles you want to use across all users.
- **params**
  - These are the url parameters. For example, you can get the username, the pageName, the itemId from here.
- **query**
  - This is an object with the all the query parameters in the url.
- **pathname**
  - This is the current url's pathname.
- **currentItem**
  - If you're at a route like `/john/tasks/3456`, this will be the item in john's data that matches the id `3456`. If no item matching this id is found or you're not at that type of route, this variable will be `undefined`.
- **parentItem**
  - This is the object that's above `currentItem` in the data. This is useful if you are letting the user browse their data hierarchically and you need to go up a level to the previous item.
- **flashErrors**
  - If there are any errors from the previous interaction (e.g. wrong password when signing in), they'll be stored in this array so they can be displayed on the page.
- **flashSuccesses**
  - If there are any success messages from the previous interaction, they'll be stored in this array so they can be displayed on the page.
- **currentUser**
  - This is an object with the current user's details in it. You can find their username like this: `currentUser.details.username` and their app data like this: `currentUser.appData`.
- **pageAuthor**
  - This is available only if you're at route like `/john` or `/kate`, with a username in it. If you are, this variable will contain the data of user that matches this username. It may be equal to the currentUser.
- **isPageAuthor**
  - This is true if the currentUser is also the pageAuthor.
- **pageHasAppData**
  - This is true if you're on a page like `/john` or `/kate`. Data is loaded from their JSON file database, so it's available on this page. If there's a `pageAuthor` variable, this will be set to `true`.


### Extra helpers

Remake also ships with all [188 Handlebars Helpers](https://github.com/helpers/handlebars-helpers), so you can have lots of flexibility with how you render your data.
