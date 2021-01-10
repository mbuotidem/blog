---
layout: post
author: Isaac Mbuotidem
---
If you're working on a React app on Windows using Windows Subsystem for Linux (WSL), you might find that your app does not reflect your changes on save. 

\
To fix that, you have two options. You can run your app with 

`$ CHOKIDAR_USEPOLLING=true npm start` 

Note however, that you will need to do this every time you want to start your app. 

\
A more permanent solution is to create a `.env` file in your project directory if you don't already have one and add

`$ CHOKIDAR_USEPOLLING=true` 

to the `.env` file. 

\
Credit : [https://stackoverflow.com/a/56199112](https://stackoverflow.com/a/62942176/7179900){:class="lnk"}




