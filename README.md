# LaTeXResumeSync

This project was born out of a conglomeration of many frustrations, as explained below.

## Motivation/Problem Statement
- I am a university student that is always stretched thin for time.
- I need to constantly apply to internships, often 4/8/12 months in advance.
    - By the time job postings come out, it's simply too late.
    - I need to be able to deliver a tailored, up-to-date version of my resume at the click of a button.
- In order to cater to people's preferences, I maintain two different formats of my resume; a two-column, and a one-column.
    - Both have content baked into their layouts. Every time I need to make a change, I need to make it to both resumes. This violates [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself).
    - This is very time-consuming and I've spent entire evenings having to update my resumes. This madness needs to stop ✌️🛑
    - My information on both resumes is 99% the same, and existing solutions for different LaTeX files to pull from a single source of truth are not great if you don't use the .bib format.
- My interests are rapidly changing, and my skills are rapidly growing. This causes me to have to change my resumes often.
- I used to make my resumes on Microsoft Word and Google Docs. However they are far too limited in terms of customizability, and look very generic.
    - Word processing software is ideal for one-dimensional, linear layouts of information; and you start to hit limits with them quickly when trying to make minor formatting/layout changes across multiple axes.
    - You constantly need to fight the architecture of the software + the template, and sometimes you don't even know which one it is 😡💢
    - Also, the templates just look bad, and get absolutely blown out the water pretty quickly by resume maker templates, Canva and Figma templates, and of course; LaTeX templates 😍
- I tried resume maker solutions such as [Resume.io](https://resume.io), [Resume.com](https://resume.com), [Resumegenius](https://resumegenius.com/), etc.
    - While they do give you a very rich selection of templates to choose from with a WYSIWYG editor, they rapidly run into customizability limitations as well; and can sometimes be even less customizable than word processing software.
    - A single template never fits all my needs. I end up searching across different templates to identify elements that I'd like to combine into one that does fit my needs; but it's impossible because the templates weren't architected to interact with each other.
    - Another crushing limitation is that in particular platforms/templates you can't always hyperlink/format specific words, which is something I do heavily in my resumes.
    - Womp womp 😭
- I've tried [Canva](https://www.canva.com/resumes/templates/) and [Figma](https://www.figma.com/community/file/934117164739642551) resumes, which I must say look gorgeous 💯
    - They are infinitely customizable, which is no surprise because that is exactly what design software is made for.
    - Canva falls short at the content management part however. Figma crushes this requirement with its component-driven architecture ✅
    - But are they ATS friendly? Nobody knows 🤷‍♂️ I personally don't even care because I believe it's not your resume + blind mass applications that get you fulfillment in life. It's finding your mission and purpose, developing the skillsets to fullfill that purpose, and letting people reach out to you if their purpose aligns with yours 🙂
    - I also don't really need the templates that they offer because I've struck gold with my content formatting and the templates I currently have. 
        - I will likely use these templates for the forseeable future, and need to be able to apply pixel-perfect customizations within LaTeX code; which is where all resume makers fall short.
        - I've been making resumes for years and have attended many resume workshops. I have never found a single template that is up to my standard and meets my needs exactly.
    - There is also but one MAJOR catch. The content is not stored in a format that is easy to import/export 😤
        - Click each element with a mouse to copy paste or try to string together plugins to fill the void? No thanks 🙅‍♂️
     
I love tables so here's a table to visualize the comparisons.

| Feature                           | Microsoft Word | Google Docs | Resume Makers | Canva | Figma | LaTeX |
|:----------------------------------|:--------------:|:-----------:|:-------------:|:-----:|:-----:|:-----:|
| Available templates               |      ✅        |     ✅      |      ✅       |  ✅   |  ✅   |  ✅  |
| Granular customizability          |      ❌        |     ❌      |      ❌       |  ✅   |  ✅   |  ✅  |
| ATS Friendly                      |      ✅        |     ✅      |      ❌       |  ❌   |  ❌   |  ✅  |
| Single source of truth for content that is easy to import/export|      ❌        |     ❌      |      ❌       |  ❌   |  ❌   |  ❌  |


## Steps I've taken to address the problem, and why they're not good enough

- I made the investment of learning LaTeX and couldn't be happier.
    - It's paying off its dividends immensely by allowing me to achieve the same level of granular control over my resume as design tools.
    - While that granular control comes at a speed cost, the ATS friendlyness and integration with single-source of truth for content is non-negotiable.

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
     - I also use [Simplify](https://simplify.jobs/) to apply to jobs, so I have to update my resume there as well.

## Immediate steps I need to complete to address the majority of the problem

This project could easily blow up into something massive and I'll probably end up trying to replace Resumake, which is not my intention. I have a limited amount of time on my hands, and need to prioritize tasks that have the greatest value. Currently, the majority of my time is spent on making content updates across the two resumes, and manually uploading them to Google drive.

- Get resumes off Overleaf onto a local directory.
- Investigate the best format in which to store my data for both resumes, including any differences. JSON? YAML? CSV?
    - It needs to be human readable, editable, and convertable to LaTeX.
    - Possibly using [Sanity](https://www.sanity.io/) as a content lake that can serve as a single source of truth for my GitHub README, Personal Portfolio Website, and my resume.
    - The ideal outcome is that I don't have to write any LaTeX code for content. I'm okay with having to modify the LaTeX templates for spacing, that's a rare task that cannot be automated because it's heavily dependent on the content.
- Write a script that uses the [Google Drive API](https://developers.google.com/drive/api/guides/about-sdk) to update the file versions whenever a change is detected.

## Nice to have so that the problem is solved once and for all
- Automate the process of uploading resumes to simplify.
- Move off LaTeX and just code out the resume in a web app that the user can interact with.


## Additional Thoughts
- This project is NOT a replacement for [Resumake](https://latexresu.me/), which is a great project you should check out.
    - While Resumake is a step in the right direction and I've considered forking it, it's far from ideal for my needs as it still runs into the same shortcomings as general resume maker solutions.
    - As the project and its userbase grows, so will the feature requests and the time/effort to maintain it, so they will likely have to incorporate premium features. It's better that I start this project now rather than later after I get locked in with them.
- I would like to grow my skills in the domain of back-end development, and this is an excellent opportunity.
    - I refuse to follow code-along tutorials and make cookie-cutter projects.
        - They don't really solve any real problems, and become abandonware that will not be maintained.
    - I prefer to learn by reading documentation and coming to my own conclusions.
        - I learn much faster. Videos are too slow and/or skip over the difficult parts.
        - You don't get to skip the difficult parts in real life.
            - There will be times when you will feel like throwing your monitor across the room. Better to feel it now than later.
        - I figure out the best practices along the way, and the knowledge sticks far better.
    - This is a project that that does solve a problem, and needs to solve it well.
        - I have no other choice but to maintain it and provide the best possible experience, because this is something I actively use.
    - I considered getting this project started as a hackathon submission, but this is too niche of a problem to have a meaningful impact on society.
- Why I wrote all this?
    - So that I myself could get clarity on EXACTLY what I want to accomplish; when, how and why.
        - I always write a project brief for myself.
            - The process of creating that brief often allows me to get an immense amount of clarity on my objectives and even identify flaws in my approach.
            - Every single line of code is technical debt. I don't want my whole project to become technical debt because my objective wasn't exactly what I thought it was going to be.
    - Also because I've quickly come to realize that most of our problems as a society are not technical, but rather communication/requirements/objectives/agendas.
    - We often do an excellent job in the technical department, but do a very poor job around processes, project/product management, and communication.
    - Rather than having to explain this project to someone verbally, I can simply give them the link to this repo so that they can read it as a memo.
