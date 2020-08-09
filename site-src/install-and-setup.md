---
layout: layout.hbs
title: Install & Setup - Remake Framework Docs
---

<img class="image--small image--center" src="https://remake.s3.amazonaws.com/smartsharp/03.svg">

# Install & Setup

**🛠 1. Install the Remake command line tool**

```bash
npm install remake -g
```

**⚡️ 2. Generate a Remake project**

```bash
remake create <project-dir>
```

**🚜 3. Start the local server**

```bash
cd projectName
npm run dev
```

**📺 4. View your Remake app**

<br>
<a href="http://localhost:3000" target="_blank"><img class="border rounded image--small image--center" src="/static/kanban-screenshot.png"></a>
<br>

Go to [http://localhost:3000](http://localhost:3000) in your browser to view the example app.

**🎨 5. Make your own app**

The HTML & CSS used to create a Remake app is in the `app/` directory.

To start from scratch with an blank slate, simply replace the files in `app/` with the files in `_remake/empty-project/`.

**👩‍🎓 6. Learn Remake**

Learn how to create an app from [the official step-by-step tutorial](https://docs.remaketheweb.com/introducing-remake/).

In no time, you'll be making web apps faster than ever!

**🌏 7. Deploy your app**

After you're done creating your own app, share it with the world:

```bash
remake deploy
```

This will publish your app to **https://YOUR-APP-NAME.remakeapps.com** and you can share it with anyone!

See an example: [https://kanban.remakeapps.com/](https://kanban.remakeapps.com/)

