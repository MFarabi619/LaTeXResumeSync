# LaTeXResumeSync

This project was born out of a conglomeration of many frustrations, as explained below.

## Motivation/Problem Statement
- I am a university student that is always stretched thin for time.
- I need to constantly apply to internships, often 4/8/12 months in advance.
    - By the time job postings come out, it's simply too late.
    - I need to be able to deliver a tailored, up-to-date version at the click of a button.
- In order to cater to people's preferences, I maintain two different formats of my resume; a two-column, and a one-column.
    - Both have content baked into their layouts. Every time I need to make a change, I need to make it to both resumes. This violates [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself).
    - This is very time-consuming and I've spent entire evenings having to update my resumes. This madness needs to stop ✌️🛑
    - My information on both resumes is 99% the same, and existing solutions for different LaTeX files to pull from a single source of truth are not great if you don't use the .bib format.
- My interests are rapidly changing, and my skills are rapidly growing. This causes me to have to change my resumes often.
- I used to make my resumes on Microsoft Word and Google Docs. However they are far too limited in terms of customizability, and look very generic.
    - Word processing software is ideal for one-dimensional, linear layouts of information; and you start to hit limits with them quickly when trying to make minor formatting/layout changes.
    - You constantly need to fight the architecture of the software + the template, and sometimes you don't even know which one it is 😡💢
    - Also, the templates just look bad, and get absolutely blown out the water pretty quickly by resume maker templates, Canva and Figma templates, and of course; LaTeX templates 😍
- I tried resume maker solutions such as [Resume.io](https://resume.io), [Resume.com](https://resume.com), [Resumegenius](https://resumegenius.com/), etc.
    - While they do give you a very rich selection of templates to choose from, they rapidly run into customizability limitations as well; and can sometimes be even less customizable than word processing software.
    - Womp womp 😭
- I've tried [Canva](https://www.canva.com/resumes/templates/) and [Figma](https://www.figma.com/community/file/934117164739642551) resumes, which I must say look gorgeous 💯
    - They are infinitely customizable, which is no surprise because that is exactly what design software is made for.
    - Canva falls short at the content management part however. Figma crushes this requirement with its component-driven architecture ✅
    - But are they ATS friendly? Nobody knows 🤷‍♂️ I personally don't even care because I believe it's not your resume + blind mass applications that get you fulfillment in life. It's finding your mission and purpose, developing the skillsets to fullfill that purpose, and letting people reach out to you if their purpose aligns with yours 🙂
    - I also don't really need the templates that they offer because I've struck gold with my content formatting and the templates I currently have. 
        - I will likely use these templates for the forseeable future, and need to be able to apply pixel-perfect customizations within LaTeX code; which is where all resume makers fall short.
        - I've been making resumes for years and have attended many resume workshops. I have never found a single template that is up to my standard and meets my needs exactly.
    - There is also but one MAJOR catch. The content is not stored in a format that is easy to migrate off of 😤
        - Click each element with a mouse to copy paste or try to string together plugins to fill the void? No thanks 🙅‍♂️
     
I love tables so here's a table.

| Feature                           | Microsoft Word | Google Docs | Resume Makers | Canva | Figma | LaTeX |
|:----------------------------------|:--------------:|:-----------:|:-------------:|:-----:|:-----:|:-----:|
| Available templates               |      ✅        |     ✅      |      ✅       |  ✅   |  ✅   |  ✅  |
| Granular customizability          |      ❌        |     ❌      |      ❌       |  ✅   |  ✅   |  ✅  |
| ATS Friendly                      |      ✅        |     ✅      |      ❌       |  ❌   |  ❌   |  ✅  |
| Single source of truth for content|      ❌        |     ❌      |      ❌       |  ❌   |  ❌   |  ❌  |


## Steps I've taken to address the problem, and why they're not good enough

- I made the investment of learning LaTeX and couldn't be happier.
    - It's paying off it's dividends immensely by allowing me to achieve the same level of granular control over my resume as design tools.
    - While that granular control comes as a speed cost, the ATS friendlyness and integration with single-source of truth for content is non-negotiable.

- Because I want to be able to easily manage my LaTeX files regardless of location or machine, I use [Overleaf](https://www.overleaf.com/).
    - Unfortunately their [Git/GitHub integration](https://www.overleaf.com/learn/how-to/Git_Integration_and_GitHub_Synchronization) is a premium feature. No thanks.
    - But thanks for motivating me to start this project and grow my skills to find a workaround.
    - [It's also open-source](https://github.com/overleaf/overleaf/wiki), and GitHub integration may be possible if I run a local instance of it.
        - This way I also don't have to set up the rendering UI myself and would save a lot duplicate effort. To be investigated 🤔🧐

- I make my edits for both resumes on OverLeaf, and then download the pdfs. I first have to delete any existing pdfs in my machine's downloads folder so that the new resumes don't have an annoying `(1)` after them 😤

- Once a resume is exported to a PDF and sent via email, it is a snapshot of my skills and experience at that time rather than being a living, up-to-date document. In order to address this, I uploaded my file to Google Drive:
![image](https://github.com/MFarabi619/LaTeXResumeSync/assets/54924158/8e342a37-0aab-4c05-802d-1a81a67ff5f4)

Then clicked on `Manage Versions`, then uploaded my new resume, so that I don't have to deal with stuff like this 👉 `resume_version_34_final_I_swear(42)` 🤣

![image](https://github.com/MFarabi619/LaTeXResumeSync/assets/54924158/1f33cf58-b060-4f49-a7ad-cd69117700cd)


The fact that a lot of people don't know this is a feature that Google Drive has blows my mind but that's a conversation for another day 💭

- Now I have my resume hosted on a google drive link, which is much easier to share than a pdf (hyperlink, QR code, etc). It will also always contain the latest version of my resume. 
     - However this whole process is repetitive, very tedious, tiring, time-consuming, and error-prone.

## Steps I need to complete to address this problem once and for all
- 


What this project is NOT:
- A replacement for [Resumake](https://latexresu.me/), which is a great project you should check out. While Resumake is a step in the right direction and I've considered forking it, it's far from ideal for my needs as it still runs into the same shortcomings as general resume maker solutions. As the project and its userbase grows, they will likely have to incorporate premium features. It's better that I start this project now rather than later after I get locked in with them.
