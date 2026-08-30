Use AI, Keep Your Thinking

A student-facing educational prototype about AI-generated content.

Practical component of an MSc Artificial Intelligence dissertation, University of Stirling, 2026.


Author: Michelle Nyoni, student number 3519339. Supervisor: Professor Matt-Mouley Bouamrane.

1. What this is

A single web page with six sections, built from the findings of a mixed-methods study: a survey of 48 university students and ten semi-structured interviews.

The research it comes from identified two gaps. The literature measures what students do with AI, and separately measures whether people can recognise AI-generated content, but rarely asks the same people about both. Additionally, every study reviewed produced recommendations for institutions rather than anything a student could open and use. This prototype addresses the second gap by translating findings from the study into a student-facing educational resource.

It is a prototype, not a product. There is no server, no database, no accounts and no tracking.

What the six sections do

Section	Purpose
Start here	What the site is, and three findings from the survey
Skills	Four flashcards on things worth being able to do unaided
Know the line	The AI Assessment Scale, three acceptable-use bands, the grey areas, and how to acknowledge AI
Spotting it	Three flashcards on why identifying AI content is harder than people assume
Quick check	Five questions with explanations, marked in the browser
Your turn	A link to the evaluation questionnaire, and where to look besides a chatbot

Every feature traces to a requirement identified in the study's own interview data. The evidence-to-feature mapping is in the dissertation.

2. How to run it

The prototype requires a modern web browser with JavaScript enabled. The optional speech feature requires browser support for the Web Speech API. An internet connection is only required to load the external fonts.

Nothing to install, nothing to build.

Online: open the live address above.
Offline: download index.html and open it in any browser.

The prototype was tested in Chromium 141. An internet connection is used only to fetch two fonts; without it the page works and simply falls back to the system fonts.

3. What is in this repository
File	What it is
index.html	The entire site. HTML, CSS, JavaScript and illustrations in one file
README.md	This file
4. What to edit

Everything configurable is in one block near the bottom of index.html, marked EDIT ME:

javascript
var SETTINGS = {
  formLink:        "https://forms.cloud.microsoft/e/h31JyRwu0c",
  researcherName:  "Michelle Nyoni",
  researcherEmail: "mtn00016@students.stir.ac.uk",
  supervisorName:  "Matt-Mouley Bouamrane",
  supervisorEmail: "matt-mouley.bouamrane@stir.ac.uk",
  libraryLink:     "",
  studySkillsLink: "",
  moduleLink:      ""
};

Change the text between the quotation marks. Nothing else needs touching. If formLink is left empty the questionnaire button hides itself and a note appears in its place, so the page can never be published with a dead button on it. Any of the three optional links left empty simply does not appear.

5. Provenance of code that is not my own

No frameworks, no libraries, no build step, no dependencies to install. The page is plain HTML, CSS and JavaScript. All illustrations are inline SVG written for this project.

Two typefaces are loaded from Google Fonts: Space Mono and Inter. They are linked, not copied, and both are open source. Source: https://fonts.google.com. If the fonts do not load, the page falls back to a monospace and a system sans-serif and remains fully usable.

AI-generated code. This project was developed with AI assistance at the AI Collaboration level. 

Reuse of publicly available code is not academic misconduct provided the source is acknowledged, which this section does.

6. Documentation of AI use

AI was used during development at the level permitted for this project. The use of AI-generated code is documented in AI_USE.md, including the tools used, relevant prompts and my review of the generated material.

Authorship marked in the code. index.html opens with an authorship record naming what was generated, by which tool, when, and who reviewed it. 

7. Data

The site stores nothing and sends nothing. There is no server, no database, no cookies and no browser storage. Text typed into the quiz reflection box and the declaration box never leaves the visitor's machine, and is gone when the tab closes. The quiz is marked in the browser and the result is not recorded anywhere.

All research data is collected through Microsoft Forms, in the researcher's University of Stirling account, as described in the approved ethics application. The site's only role is to link to it.

No personal data is requested at any point, on the site or in the questionnaire: no name, student number, email address or date of birth.

8. Known limitations
At the time of this version, the prototype has been implemented but its effectiveness as an educational resource has not yet been established through user evaluation. The evaluation questionnaire is provided separately for this purpose. It can report how many participants identified each correctly, but it cannot test whether judgement transfers between everyday and academic settings. The self-rating items measure belief about ability rather than ability itself.
The two passages differ in sentence rhythm as well as in origin, so responses to them cannot be attributed to origin alone.
The prototype was tested in Chromium only; compatibility with other browsers was not formally evaluated.
The site is not a detection tool and does not claim to identify AI-generated content. This is deliberate: the study's own interview data raised both the unreliability of detectors and the harm of false accusation.
The acceptable-use bands are a plain-language illustration, not any institution's policy, and the page says so.
9. Accessibility notes
The listen button uses the browser's own speech synthesis. No audio files are downloaded. Voices vary by device, and the button reports it plainly if the browser has none.
Right and wrong in the quiz are signalled by the words "Correct" and "Not quite" as well as by colour, so nothing depends on colour alone.
The acceptable-use tiles open on hover with a mouse and on tap on a touchscreen.
The page reflows to a single column below 760 pixels.
