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
    <img src="https://troglio.com/img/trello-blog-board.png" alt="Troglio" />
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

Go to [Trello.com](https://trello.com), add the `Troglio` power-up to a board, and dollow the getting started !


# Push or Pull ?

After connecting Troglio to your Trello account, you are asked to setup a destination for your data. By default, Troglio only **pushes** data to this destination. If you prefer **pulling** data, you can easily send them to a server you can pull from. There are two different approches for that:
1. Send data to a git repository, like github, that will trigger a CI build responsible for publishing `.json` files (to github pages, gitlab pages...).
2. Send data to a custom server accepting POST requests, store data, then serve them through an API. [Here is an Express project for you to get started](https://github.com/Troglio/express-nedb-endpoint).

# Previews

Previews is a neat feature that allows one to instantly see changes before publishing them live. This is not a mandatory option, but is for sure a must-have for writers and marketers. It requires a separate **url** to be setup. The **url** is nothing more than the domain of the website. For example, if the final website lives at `https://mydomain.com`, just put this **url** in the related setup (by clicking the `Preview` button in any card for the first time, or by going in the power-up's settings).

**How it works ?**
Basically, Troglio processes and transforms data right in the browser. When user requests a preview, Troglio opens an iFrame containing both the corresponding page + the new data.

As a developper, it means you have to prepare each pages to receive those data to fill your templates live. If you use a Javascript framework (like React), it is just a piece of cake: just prepare routes to receive data when the page is opened in an iFrame and request the data. [Here is a complete working project for you to get started.](https://github.com/Troglio/troglio-starter-preact-static)


# Support
This is a nice place to keep technical problems centralized :)
If you have any problems related to developping apps and websites with troglio, please just fill an issue here.

