---
title: "Serving Unity WebGL Builds from Github Pages"
date: 2017-10-10
excerpt: "In addition to supporting PC, Mac, Linux, iOS, Android, and others, Unity supports building for WebGL, which allows developers to host Unity games on the internet.  Github Pages is a powerful platform for serving static content.  Used together, it is easy to maintain a simple website which serves playable games."
categories:
  - General
tags:
  - about
  - jekyll
  - github pages
  - unity
---

<style type="text/css">
  #partners {
    height: 105px;
    background-color: #eee;
    white-space: nowrap;
    width: 100%;
    display: table;
  }

  .logo-image {
    vertical-align: middle;
    padding: 13px;
    display: table-cell;
  }
  
  .logo-image img {
    max-width: 100%;
  }
</style>

<div id="imageGroup">
  <div class="logo-image">
    <img src="https://upload.wikimedia.org/wikipedia/commons/8/8a/Official_unity_logo.png" alt="" />
  </div>
  <div class="logo-image">
    <img src="https://assets-cdn.github.com/images/modules/logos_page/Octocat.png" alt="" />
  </div>
  <div class="logo-image">
    <img src="https://jekyllrb.com/img/logo-2x.png" alt="" />
  </div>
</div>

WIP - I'll add more detail to this soon.


In addition to supporting PC, Mac, Linux, iOS, Android, and others, Unity supports building for WebGL, which allows developers to host Unity games on the internet.  Github Pages is a powerful platform for serving static content.  Used together, it is easy to maintain a simple website which serves playable games.

Disclosure: I am new to Jekyll (the site generator/templating engine powering Github pages) and don't promise this is easiest or most extensible way to solve this problem.

Step 1) Set up a site using Github Pages.  I forked [minimal-mistakes](https://github.com/mmistakes/minimal-mistakes) to get started because I like the clean look-and-feel.  Play around until you are comforatable adding posts, and see the [referenced documentation](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/) as needed.

Step 2) Build your unity project for WebGL, preferrably not using 'development mode'.  (link to info) This will produce a directory containing `index.html`, `Build/`, and `TemplateData/`.

Step 3) Commit the `Build/` and `TemplateData/` directories to `/assets/unity/build_name/` in your project (change 'build_name' to whatever you want the name of your build to be)

Step 4) Create a post and add this snippet to front matter:  `unity_dir: build_name` using your build_name from before

Step 5) update the layout (give the layout)

Step 6) add the page for unity (give the page v1)

Step 7) make sure your site baseurl is set

Step 8) load your page.  hopefully you see a build loading.  if not, use chrome's developer tools to right-click where the game should be, and pull up the inpsector.  Confirm the path for your different game assets is what you expect it to be.  If not you may need to do some trouble shooting (feel free to comment below if you get stuck, preferrably including a link to your repo, and I'll try to help)

You are serving your Unity game from github, which is awesome.  It would be nice if the game didn't load as soon as the page loads though.  Lets fix that.
Step 9) We're going to add a button that loads the game when pressed, and displays an image of the game. (give the page v2)
Step 10) Lets display the same game image on the main list for the posts (give archive-single changes - the 'grid' removal, and the setting of teaser)

And that's it.
I'll be updating this post with more detailed instructions.

Check out the next post for a working example.
