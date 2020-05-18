---
title: Getting setup with .Net Core, MonoGame and SadConsole
description: Creating a new dotnet core & C# project using SadConsole template.
date: 2020-05-17
tags:
  - csharp
  - SadConsole
  - roguelike
layout: layouts/post.njk
---

I did this on both MacOS and Linux and it was crazy easy.

## Just follow the instructions

There's a [**guide**](https://sadconsole.com/articles/getting-started-sadconsole-core-cli-template.html) on the SadConsole website which explains what you need to do to create a new project. There isn't anything about the guide that's specifically for Windows, just follow the instructions if you're on MacOS or Linux.

<span style='font-weight:700;color: #FF0000;'>STOP!</span> seriously read the [**guide**](https://sadconsole.com/articles/getting-started-sadconsole-core-cli-template.html) and you should see random garbage on a console view. Anything else I've written is 100% based off the guide, I have nothing new to add.

Summary of installation instructions:

1. [Install .Net Core](https://dotnet.microsoft.com/download/dotnet-core) (Version 3.1 at the time I wrote this)
1. [Install MonoGame](https://www.monogame.net/downloads/) (3.7.1 when I wrote this)
1. Creating a working folder and change directory into it
1. Install the [SadConsole.Templates](https://sadconsole.com/articles/getting-started-sadconsole-core-cli-template.html#install-the-templates) (this will work across operating systems)
1. [Create a project](https://sadconsole.com/articles/getting-started-sadconsole-core-cli-template.html#create-a-project)
1. Run the project with `dotnet run`

If everything worked you should see this:

![SadConsole view of random garbage](/img/hello_from_sadconsole.png)
