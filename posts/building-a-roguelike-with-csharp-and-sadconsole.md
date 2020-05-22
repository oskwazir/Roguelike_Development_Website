---
title: Writing a roguelike with C# and SadConsole
description: Converting a Java rogulike tutorial to C# and SadConsole.
date: 2020-05-18
tags:
  - csharp
  - SadConsole
  - roguelike
  - tutorial
layout: layouts/post.njk
---

I want to convert [Trystan's roguelike tutorial](http://trystans.blogspot.com/) to use C# and SadConsole. Since my C# knowledge is a bit outdated (by nearly a decade) I will update any code when I know better.

I just want to get started building *something* so anything is a good enough start. If you haven't created a basic SadConsole project yet, it would be best to start [here](/posts/getting_started_with_dotnet_core_monogame_and_sadconsole/).

I'm using JetBrains Rider as my IDE. A lot of people use Visual Studio Code, it doesn't really matter what you're using to follow along.

# Outline

Create a new project using the sadconsole template.
```shell script
# Create a new directory with two child folders
mkdir -p  RoguelikeTutorial/{src,test}
cd RoguelikeTutorial
git init
dotnet new gitignore  

cd RoguelikeTutorial/src
dotnet new sadconsole8 -o RoguelikeTutorial

cd ../test
dotnet new xunit -o RoguelikeTutorial.Tests

cd RoguelikeTutorial.Tests
dotnet add reference ../../src/RoguelikeTutorial/RoguelikeTutorial.csproj

cd ../..

# Create a Solution file
dotnet new sln

# Add the RoguelikeTutorial and RoguelikeTutorial.Tests project so we can easily
# build and run tests
dotnet sln add src/RoguelikeTutorial/RoguelikeTutorial.csproj
dotnet sln add test/RoguelikeTutorial.Tests/RoguelikeTutorial.Tests.csproj

# now make sure the solution file can build both the game and tests
dotnet build

# run all tets, there's only the one example test
dotnet test

# Let's make sure the game will run
cd src/RoguelikeTutorial
dotnet run
#You should see the random color garbage screen
git add -A
git commit "First commit"

#And we are ready to start.
```
Git init.
Add a gitignore file for C# and Rider.
Create a repo on your favorite git site
Push the initial commit up.
run the project to make sure it works

## Extra
Setup unit tests for C#
Since I'm using Github, I'll create a Travis.CI file so I can run unit tests on each push/PR.


