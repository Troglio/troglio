<p align="center">
    <img src="https://troglio.com/img/troglio-logo.png" width="200" height="200" alt="Troglio" />
</p>
<br />

# Troglio

Turn Trello into a fully fledged CMS: pages, posts, custom types, previews... and more !
<br />
Look how your next website backend could look-like:
<br />
<p align="center">
    <img src="https://troglio.com/img/trello-blog-board.png" alt="Trello Blog board example" />
</p>

# Features
- :electric_plug: Connect to any site or app.
- :beach_umbrella: Write from anywhere, even offline.
- :mag_right: Instant previews: visualize your changes live.
- :arrows_counterclockwise: Push or Pull data: your choice.
- **M** Write using Markdown.
- :bookmark: Add custom properties using Custom fields (separate power-up) and/or a TOML-like syntax.
- :video_game: Don't repeat yourself: control properties from other cards.

# Starters & Tutorials

- [A basic blog with Trello](https://github.com/Troglio/troglio-starter-preact-static)
- [A minimal API endpoint with Node.js + Express + Nedb](https://github.com/Troglio/express-nedb-endpoint)


# Getting started

Go to [Trello.com](https://trello.com), add the `Troglio` power-up to a board, and follow the getting started !

<br />
<p align="center">
    <img src="https://troglio.com/img/enable-troglio-power-up.gif" alt="Enable troglio power-up" />
</p>


# Push or Pull ?

After connecting Troglio to your Trello account, you are asked to setup a destination for your data. By default, Troglio only **pushes** data to this destination. In most cases, this is fine because one can take advantage of CI pipelines to trigger builds whenever new data arrives in their git.

However, if you prefer **pulling** data, you can easily send them to a server that will act as your API endpoint. There are two different approches to do that:
1. Send data to a git repository, like github, that will trigger a CI build responsible for publishing `.json` files (to github pages, netlify, or any CDN...).
2. Send data to a custom server accepting POST requests, that will store data then serve them through a JSON API. [Here is an Express project for you to get started](https://github.com/Troglio/express-nedb-endpoint).

# Previews

Previews is a neat feature that allows one to instantly see changes before publishing them live. This is not a mandatory option, but is for sure a must-have for writers and marketers. For it to work, it requires a separate **url** to be setup. The **url** is nothing more than the **domain** of the website. For example, if the final website lives at `https://mydomain.com`, just put this **url** in the related setup (by clicking the `Preview` button in any card for the first time, or by going in the power-up's settings).

**How it works ?**
Basically, Troglio will create JSON pages out of Trello cards right in the browser. When a user requests a preview, Troglio opens an iFrame containing both the corresponding page + the new data.

As a developer it means that, when your website is opened through an iFrame, you should intercept these new data and propagate them accordingly to fill your templates lives.

If you use a Javascript framework (like React), it is a piece of cake: just catch the new data and propagate them into your routes as new props. [Here is a complete working project for you to get started.](https://github.com/Troglio/troglio-starter-preact-static)


# Support
This is a nice place to keep technical problems centralized :)
If you have any problems related to developping apps and websites with troglio, please just fill an issue here.

