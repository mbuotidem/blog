---
layout: post
author: Isaac Mbuotidem
---
If you're working on a React app on Windows using Windows Subsystem for Linux (WSL), you might find that your app does not reflect your changes on save. 

Your first step to fixing this is to ensure that your React files are located on the WSL filesystem and not the Windows filesystem. For example, if your files are saved at : 

`C:Users\yourusername\Documents\test-react-app`

Use the `cp` command to copy them over to your WSL filesystem like so:

`cp -r /mnt/c/Users/yourusername/Documents/test-react-app ~/test-react-app`. 

The above will copy the files to your WSL user account's home directory which you can always get to by typing `wsl ~` from `Command Prompt` or `Windows Terminal`. 

If that still does not work, try running your app with: 

`$ CHOKIDAR_USEPOLLING=true npm start` 

Note however, that you will need to do this every time you want to start your app. 

\
A more permanent solution is to create a `.env` file in your project directory if you don't already have one and add

`$ CHOKIDAR_USEPOLLING=true` 

to the `.env` file. 

\
Credit : [https://stackoverflow.com/a/56199112](https://stackoverflow.com/a/62942176/7179900){:class="lnk"}




