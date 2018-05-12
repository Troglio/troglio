<p align="center">
    <img src="https://troglio.com/img/troglio-logo.png" width="200" height="200" alt="Troglio" />
</p>
<br />

# Troglio

Turn Trello into a fully fledged CMS: pages, posts, custom types, previews... and more !
<br />
See how your next website backend could look-like:
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

First you need to add Troglio as a custom power-up.

For this, you need to go to [your power-up's admin interface](https://trello.com/power-ups/admin) to add a new Power-Up.
If you didn't created a team yet, you can create one now (Power-Ups need a team).
Once you selected your team, just click on "Create a new Power-Up", fill the form like this:

**Power-Up name:** Troglio

**Author name:** troglio

**Email:** team@troglio.com

**Overview:** Turn Trello into a CMS

**Description:** # Power your apps and websites from Trello

**Category 1:** Marketing & Social Media

**Category 2:** Developers Tools

**Power-Up capabilities:** authorization-status, board-buttons, callback, card-buttons, show-authorization, show-settings

**Power-Up icon URL:** https://powerup.troglio.com/troglio-logo.png

**iFrame connector URL:** https://powerup.troglio.com/index.html

**Link to your privacy policy:** https://troglio.com/privacy

**Support team email:** support@troglio.com


Once you have added the Power-Up, you are good to go !! Just go to any board in the selected team and add your custom Power-Up named Troglio:

<br />
<p align="center">
    <img src="https://troglio.com/img/enable-troglio-power-up.gif" alt="Enable troglio power-up" />
</p>

# Why Troglio is not available directly into Trello ?!

We presented Troglio in front of Trello and received a very good attention and interest. However, we agreed upon the fact that Troglio is a bit more advanced than the average Power-Up. Precisely, **Troglio is out of the scope of Trello's average user base since the user needs to already come with its app/website to find an interest in using Trello/Troglio**.

We do aknowledge the fact that Troglio has extensive flexibility overwhelming the average click-and-point user. However, apps and websites are never done without an advised technician able to [read our docs](https://troglio.com/guide) and do the proper setup for its customer/fellow writer. After setup, Troglio is made for average user to be more than comfortable to edit and organize its content intuitively (it's just text and images in Trello cards: setup makes the rest automagically). 

That being said, Troglio is not meant to be a drop-in replacement for Wordpress and other CMS, rather it is a neat way for developers to stay away from monolothic CMS and suggest customers a JAMStack-style exprience: developers do what they are good at without limits, and users edit their content free from any organizational constraints.

Finally, note that **Trello expressely encouraged us** to promote Troglio this way (out of Trello) since our direct audience is **YOU** (advanced user) before the average Trello user: we first need a website/app for troglio to make sense. Having the power-up available from their public listing could lead to confusion, especifically if the user does not have a website/app just yet.


# The guide

Please follow the complete guide available at [troglio.com/guide](https://troglio.com/guide).


# Push or Pull ?

After connecting Troglio to your Trello account, you are asked to setup a destination for your data. By default, Troglio only **pushes** data to this destination. In most cases, this is fine because one can take advantage of Continuous Integration pipelines to trigger builds whenever new data arrives in their git.

However, if you prefer **pulling** data, you can easily send them to a server that will act as your API endpoint. There are two different approches to do that:

1. Send data to a git repository, like github, that will trigger a CI build responsible for publishing `.json` files (to github pages, netlify, or any CDN...).
2. Send data to a custom server accepting POST requests, that will store data then serve them through a JSON API. [Here is an Express project for you to get started](https://github.com/Troglio/express-nedb-endpoint).

# Previews

Previews is a neat feature that allows one to instantly see changes before publishing them live. This is not a mandatory option, but is for sure a must-have for writers and marketers. For it to work, it requires a separate **url** to be setup. The **url** is nothing more than the public **domain** of the website. For example, if the final website lives at `https://mydomain.com`, just put this **url** in the related setup (by clicking the `Preview` button in any card for the first time, or by going in the power-up's settings).

**How it works ?**
Basically, Troglio will create JSON pages out of Trello cards right in the browser. When a user requests a preview, Troglio opens an iFrame containing both the corresponding page + the new data.

As a developer it means that, when your website is opened through an iFrame, you should intercept these new data and propagate them accordingly to fill your templates, live.

If you use a Javascript framework (like React), it is a piece of cake: just catch the new data and propagate them into your routes as new props. [Here is a snippet illustrating the point](https://github.com/Troglio/troglio-starter-preact-static/blob/master/src/App.js) **(PAY ATTENTION TO COMMENTS)**.


# Support
This is a nice place to keep technical problems centralized :)
If you have any problems related to developping apps and websites with troglio, please just fill an issue here.

