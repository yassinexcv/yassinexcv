### Hi there 👋

<!--
**yassinexcv/yassinexcv** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
  - I’m currently a web developer student at YouCode School
  - I’m currently learning: Web dev, and more ...
  -   📈 My Github status


![GitHub Stats](https://github-readme-stats.vercel.app/api?username=yassinexcv&theme=radical) 
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=yassinexcv&theme=tokyonight)
![](https://visitor-badge.laobi.icu/badge?page_id=yassinexcv.yassinexcv)
[![Github](https://img.shields.io/github/followers/yassinexcv?label=Follow&style=social)](https://github.com/yassinexcv)

Skip to content
DEV Community
Log in
Create account
Cover image for Create a dynamic GitHub profile Readme
Charalambos Ioannou
Charalambos Ioannou

Posted on 3 août 2020
Create a dynamic GitHub profile Readme
#github
#markdown

GitHub recently released a feature that allows users to create a profile Readme markdown file. This has not been officially documented by GitHub but it is used by plenty of people. This profile Readme file acts like a portfolio for users and allows the users to convey important information about them to whoever is watching their profile.

There are a lot of articles which show how to create a profile readme. In this article I will describe how to make it dynamic. For example, show some GitHub profile stats (stars, commits, etc), show the most used languages or even show the most recent blog posts of the user. You can check my profile here here: https://github.com/CharalambosIoannou. Now let’s begin:
Step 1: Create the profile readme

    Go to GitHub and create a new repository with your username as the name of the repository as seen below. Also tick the box which says Initialize this repository with a README. Mine shows a warning since I have already created the repo.

Step 2: Add the details you want to show to the rest of the world

    What I did was display my name in the top along with the link to my website for easy access by anyone.
    Then I completed the default information provided by GitHub once the readme file is created.
    Then I added links to social media and contact info for anyone who wants to contact me and afterwards I added icons to all the languages and tools I frequently use and I am familiar with. The code for these is seen below: (I removed most of the language links so that it does not take much space here. If you want the full list check my readme file from the link at the end of the article)

## ✉️ Find me on:


<p align="center">
 <a href="https://charalambosioannou.github.io/" target="_blank" rel="noopener noreferrer"> <img src="https://raw.githubusercontent.com/iconic/open-iconic/master/svg/globe.svg" alt="Python" height="40" style="vertical-align:top; margin:4px"> </a>
 <a href="https://linkedin.com/in/charalambosioannou" target="_blank" rel="noopener noreferrer"> <img src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/linkedin.svg" alt="Python" height="40" style="vertical-align:top; margin:4px"></a>
 <a href="mailto:cioannou1997@gmail.com"> <img src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/gmail.svg" alt="Python" height="40" style="vertical-align:top; margin:4px"></a>
</p>

<br />

## 🧰 Languages and Tools:
<p align="center">
<img src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/python/python.png" alt="Python" height="40" style="vertical-align:top; margin:4px">
<img src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/javascript/javascript.png" alt="Javascript" height="40" style="vertical-align:top; margin:4px">
<img src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/visual-studio-code/visual-studio-code.png" alt="VS Code" height="40" style="vertical-align:top; margin:4px">
</p>

I used html style for showing the images instead of markdown because I can center the images.

    My readme profile with those details is shown below

Step 3: Add dynamic data

    The dynamic data I use are:

    1) GitHub profile visitor count
    2) GitHub profile followers count
    3) Dev.to blog posts
    4) GitHub profile statistics (stars, commits, etc)
    5) Most used languages in my repositories

1) GitHub profile visitor count

    Add this line of code to the readme but replace my username CharalambosIoannou with your github username.

![](https://visitor-badge.laobi.icu/badge?page_id=CharalambosIoannou.CharalambosIoannou)

2) GitHub profile followers count

    Add this line of code to the readme but replace my username CharalambosIoannou with your github username.

[![Github](https://img.shields.io/github/followers/CharalambosIoannou?label=Follow&style=social)](https://github.com/CharalambosIoannou)

3) Dev.to blog posts

    In order to dynamically get the latest dev.to blog posts we have to create a YAML file and a GitHub action, however thanks to this repo https://github.com/gautamkrishnar/blog-post-workflow this has never been easier.
    The first step to do this is to copy and paste this code section inside your readme file:

# Blog posts
<!-- BLOG-POST-LIST:START -->
<!-- BLOG-POST-LIST:END -->

    The next step is to create a folder named .github and inside that create another folder named workflows.
    In the workflows folder create a file named blog-post-workflow.yml
    In the blog-post-workflow.yml file copy and paste this code:

name: Latest blog post workflow
on:
  schedule:
    # Runs every hour
    - cron: '0 * * * *'
  workflow_dispatch:

jobs:
  update-readme-with-blog:
    name: Update this repo's README with latest blog posts
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: gautamkrishnar/blog-post-workflow@master
        with:
          feed_list: "https://dev.to/feed/charalambosioannou"

    In the feed_list section replace my dev.to username charalambosioannou with your own dev.to username.

    There are a lot of other settings here like changing the number of posts shown (the default is 5) or adding multiple sources (dev.to, stackoverflow,etc). All these settings can be found here: https://github.com/gautamkrishnar/blog-post-workflow#options

    Then push your changes if you have done them locally and go to the actions section.

Alt Text

    The next step is to click on the Latest blog post workflow button, then Run workflow and again Run workflow. Then wait a few seconds and the task will run.

4) GitHub profile statistics (stars, commits, etc)

    Add this line of code to the readme but replace my username CharalambosIoannou with your github username.

![GitHub stats](https://github-readme-stats.vercel.app/api?username=CharalambosIoannou&show_icons=true&theme=tokyonight)

    If you want to change the theme of the stats go to https://github.com/anuraghazra/github-readme-stats/blob/master/themes/README.md and choose the theme you like and replace the tokyonight text in the url with the name of the theme you want.

5) Most used languages in my repositories

    Add this line of code to the readme but replace my username CharalambosIoannou with your github username.

![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=CharalambosIoannou&theme=tokyonight)

    If you want to change the theme of the stats go to https://github.com/anuraghazra/github-readme-stats/blob/master/themes/README.md and choose the theme you like and replace the tokyonight text in the url with the name of the theme you want.
    You can also hide a language by adding the parameter &hide=language in the url. Replace language with the language name you want to hide.

Conclusion

The end result looks like this:
Alt Text

I suggest for your own profile to make it concise and be creative with it. I hope you enjoyed this tutorial and found it useful. You can check mine here: https://github.com/CharalambosIoannou. If you need some ideas on how to create your own readme you can find plenty of examples in this repo: https://github.com/abhisheknaiidu/awesome-github-profile-readme

I hope you enjoyed reading this article and found the content helpful. You can support me by clicking the button below to buy me a cup of coffee. Your generosity will encourage me to write articles more frequently.

Buy Me A Coffee
Discussion (0)
pic
Code of Conduct • Report abuse
Read next
dillonb07 profile image
Access GitHub GraphQL queries easily in Python

Dillon Barnes - Feb 21
richkurtzman profile image
How our micro frontends help businesses big and small

Rich Kurtzman - Feb 15
gaelgthomas profile image
How to Deploy a Static Website for Free Using Github Pages

Gaël Thomas - Feb 28
jhonywalkeer profile image
GitHub - Pacote do Desenvolvedor Aluno (De graça)

Jhony Walker - Feb 15
Charalambos Ioannou
MSc Data Science student at the University of Edinburgh. Also intersted in Machine learning and Deep Learning.

    Location
    Edinburgh, UK
    Education
    Durham University
    Joined
    16 mai 2020

More from Charalambos Ioannou
Create a static webpage with a contact form on Github pages
#webdev #github #beginners

## ✉️ Find me on:


<p align="center">
 <a href="https://charalambosioannou.github.io/" target="_blank" rel="noopener noreferrer"> <img src="https://raw.githubusercontent.com/iconic/open-iconic/master/svg/globe.svg" alt="Python" height="40" style="vertical-align:top; margin:4px"> </a>
 <a href="https://linkedin.com/in/charalambosioannou" target="_blank" rel="noopener noreferrer"> <img src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/linkedin.svg" alt="Python" height="40" style="vertical-align:top; margin:4px"></a>
 <a href="mailto:cioannou1997@gmail.com"> <img src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/gmail.svg" alt="Python" height="40" style="vertical-align:top; margin:4px"></a>
</p>

<br />

## 🧰 Languages and Tools:
<p align="center">
<img src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/python/python.png" alt="Python" height="40" style="vertical-align:top; margin:4px">
<img src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/javascript/javascript.png" alt="Javascript" height="40" style="vertical-align:top; margin:4px">
<img src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/visual-studio-code/visual-studio-code.png" alt="VS Code" height="40" style="vertical-align:top; margin:4px">
</p>

DEV Community — A constructive and inclusive social network for software developers. With you every step of your journey.

Built on Forem — the open source software that powers DEV and other inclusive communities.

Made with love and Ruby on Rails. DEV Community © 2016 - 2022.
