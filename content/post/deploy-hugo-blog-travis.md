---
title: "Automatically Deploy a Hugo Site to GitHub Pages using Travis CI"
date: 2019-08-04T13:59:01+01:00
Description: ""
Tags: ['hugo','ci','travis','github']
Categories: []
Draft: true
author:
  given_name: Ben
  family_name: Crisp
  display_name: Ben Crisp

---

## Introduction

This post explains how I use Travis CI to automatically build and deploy a static webiste created with Hugo to my GitHub Pages repository. 

## GitHub Pages

[GitHub Pages](https://pages.github.com/) allows you to host a static website directly from a GitHub repository (for free!). 

Pages has built-in support for [Jekyll](https://jekyllrb.com/), a popular [static site generator](https://stackoverflow.com/questions/30181349/what-is-a-static-site-generator). This integration makes deploying your Jekyll site a simple `git push`. When you make changes to your site, GitHub automatically generates the public HTML files from the Jekyll source code in your repository. 

Jekyll is great, but what if you want to use one of the many other static site generators out there (like [Hugo](https://gohugo.io)) with GitHub Pages? You could simply build the site manually (it's not exaclty difficult). Or, you could use a continuous intergation service like Travis to get the same level of automation enjoyed by Jekyll users.

## Travis CI

[Travis](https://travis-ci.com/) is a free hosted [continuous intergation](https://martinfowler.com/articles/continuousIntegration.html) service. It integrtaes with GitHub to build, test and deploy code from your repositories.

When you push changes to a Travis-enabled repository, Travis will automatically undertake a series of steps (defined by you in a .travis.yml file) to build and test your code. If all the tasks succeed, the build is deemed to have "passed" and the software is deployed (e.g. to a web server). If any of the tasks should fail, the build is described as "broken" and nothing is deployed. 

Travis can notify you (e.g. by email) whenever a build passes or fails, and also provides neat little build status badges (like the one below that show the build status of this blog!).

[![Build Status](https://travis-ci.org/bcrisp4/thecrisp.io.svg?branch=master)](https://travis-ci.org/bcrisp4/thecrisp.io)

## Hugo

As previously mentioned, Hugo is a static site genrator. In fact, it is the static site generator I use for this blog!

I don't cover how to install Hugo and create a Hugo site in this post, but it is easy enough to do and is well explained in the official [Install Hugo](https://gohugo.io/getting-started/installing) and [Quick Start](https://gohugo.io/getting-started/quick-start/) guides.


