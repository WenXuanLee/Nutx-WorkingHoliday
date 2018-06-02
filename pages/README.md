# PAGES

This directory contains your Application Views and Routes.
The framework reads all the .vue files inside this directory and creates the router of your application.

More information about the usage of this directory in the documentation:
https://nuxtjs.org/guide/routing

## Core concept

Every `vue file` in pages will be `seen as a route`，which could be nexted route or more complex route.

the route name will be the file name

* 即使是在目錄底下一樣會認外層的目錄名稱為route，也就是如果`about.vue => about dir 裡的index.vue`，route位置一樣為`/about`
