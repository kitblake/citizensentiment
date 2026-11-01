# Citizen Sentiment PRD v1

#### Metadata

Project:  Citizen Sentiment app  \
Conception: Built at the Kesennuma Hackatsuon, Sept 28 ~ Oct 10th 2026  \
Presented: October 10th, 2026  \
Presentation: https://docs.google.com/presentation/d/1MgNv7ET512Ok534cw667VMeXVcHkJLhF92t5bHKhpb8/edit?usp=sharing  \
Demo URL: https://citizen-sentiment-kesennuma.netlify.app/ja/poll  \
Demo PDF: [FlyerSetup.pdf](./FlyerSetup.pdf) (paper flyer handed out at the presentation)  \
Github repo: https://github.com/kitblake/citizensentiment/  \
Source code: https://github.com/AkakpoErnest/HaboSavey/  \
Developer: Pablo Akakpo  \
PRD doc: https://github.com/kitblake/citizensentiment/blob/main/prd.md  \
Author: Kit Blake

## Abstract

Citizen Sentiment is a simple app that enables Kesennuma city officials to gather the preferences of citizens about a future project. It’s primarily visual where images, in A/B format, are distributed in multiple media, including web, app, and paper. Promotion includes a QR code link. After citizens scan the QR code they land on a poll page in the Citizen Sentiment app. They make a choice between image A and B and submit their preference. The city can then gauge the sentiment of the populace when making decisions.

### Intended Use

Citizen Sentiment is a tool for conducting polls within Kesennuma. The poll is distributed on the existing communication channels, including the Kesennuma city website, LINE, the CrewShip app, and as a paper flyer. The flyer can be placed at local restaurants and cafes and mailed to residents at their home address. In this way the city can be certain that the poll reaches most citizens and people concerned.

In the presentation Citizen Sentiment is described as an ‘app’. However, it’s not intended to be an application on a smartphone. The poll is meant to be a feature of the city website. It functions as an app within the website.

It’s also not the intention that the app will be named Citizen Sentiment (or 市民みんなの声). That’s simply the name of the project.

### Scope of this document

This document only describes requirements for the website implementation. Other channels, like LINE or the CrewShip app, can either direct residents to the poll page with a link, or integrate the poll into the platform. Those implementations need to be determined by the responsible administrators.

<!-- ### Resources

### Roles -->


## Rationale

Kesennuma city has a strong track record in engaging citizens to participate in decision making, exemplified by the Oya Coast project. Each district has neighborhood associations which organize meetings that residents can attend. The city also keeps citizens up-to-date by sending notifications on the website, LINE, and the CrewShip app.

### Problems

- Participation in the existing city processes is time consuming for residents.
- Attendance at community meetings is low (as an example, in my city in the Netherlands, when the local neighborhood association holds a meeting, less than 1% of the residents attend).
- The notifications on LINE are one-way communication. They’re essentially a broadcast with no way for citizens to respond.
- Residents don’t feel involved in decision making or determining the future of their city.

### Solutions

Citizen Sentiment is designed to bridge the gap between active participants and interested citizens. ‘Active participants’ may attend neighborhood association meetings and invest substantial time in the process. ‘Interested citizens’ are people who would like to share their opinion with the city but don’t make time to get involved with a project.

- Citizen Sentiment disseminates polls about upcoming projects and policy decisions. Typically there is an A/B choice to vote on.
- Citizen Sentiment is a low-barrier app. No login or authentication is required. The poll is open and any individual can respond.
- By utilizing a QR code containing a web link, any citizen with a smartphone can easily scan the code and participate in the poll.
- The poll score (percentage of votes for choice A or B) is transparently shared with participants on the poll “Thank You” page.
- City officials can access a backend of the app with a more detailed breakdown of citizen participation and preferences.


## Users

### Target Audience

1. **Ordinary Citizens**
  - **Who they are**: Residents of Kesennuma city, or people who live elsewhere but work in the city.
  - **Needs**: Quick and easy access, clear guidance, immediate opportunity to vote and thereby share their opinion.
  - **Pain points**: Complex interaction with existing services, difficulty with tech, unclear community resources, limited communication from the city/district.

2. **Web Content Manager**
  - **Who they are**: City employee or freelancer responsible for Content Management of the Kesennuma city website. Tasks include managing text and image assets used in polls, scheduling polls, and organizing poll distribution across media channels.
  - **Needs**: Efficient content management processes, automated technical integrations, ability to quickly update poll and website materials, relationships with other personnel involved in poll dissemination.
  - **Pain points**: Time-consuming manual processes, repetitive technical tasks, support issues, limited capacity for creative contribution.

3. **City Officials**
  - **Who they are**: Elected officials and civil servants working in the city administration. City council members and other positions serving as liaisons or as representatives of the populace.
  - **Needs**: Access to poll results and analysis, ability to propose polls, contact with the city communications team that is responsible for the website, LINE and CrewShip app.
  - **Pain points**: Difficulty learning how citizens feel about proposed changes within the city, limited access to online feedback tools, complex internet communication systems.

<!-- 4. **Community/Support Worker**
  - **Who they are**: City employee or freelancer responsible for interacting with citizens. The worker functions as both a liaison for the city and a support contact person.
  - **Needs**: Access to communication channels (telephone, chat apps, LINE, etc). Extensive FAQ database with answers to Frequently Asked Questions. Updates about planned campaigns that may trigger support requests.
  - **Pain points**: Difficulty helping elderly or non-tech savvy citizens navigate a smartphone or website, limited technical knowledge, language barriers, non-standard work times. -->


### User Stories

- As an **Ordinary Citizen**:
  - I want to be informed about proposed changes in the city and share my opinion in a poll.
  -  I want to share my opinion effortlessly.
  -  I want to be informed about opportunities in the future to participate in a decision process.
  -  I want to learn how other residents feel about an issue.

<p></p>

- As a **Web Content Manager**:
  - I want to efficiently create polls on the city website.
  - I want to schedule polls with a start and end time.
  - I want to create a QR code containing the website address of a poll.
  - I want to create invitations to participate in a poll on the city’s communication channels.
  - I want to create a PDF for a paper version of the invitation that can be distributed as a flyer.
  - I want to manage an archive of polls that have  been conducted and are publicly viewable on the website.
  - I want to create multilingual polls.
  - I want to create polls on the website that comply with "JIS X 8341-3: 2016", compliance level AA.

<p></p>

- As a **City Official**:
  - I want to propose polls about important issues.
  - I want to engage citizens in decision making processes.
  - I want to make citizens feel like their opinions matter.
  - I want to make sharing opinions an effortless, enjoyable, and rewarding activity.
  - I want to learn how residents feel about a proposed project or policy.
  - I want to encourage citizens to play a more active role in change making processes.
  - I want to receive detailed feedback about the results of a poll.


### User Flows

- **Ordinary Citizen** participates in a poll:
  - Receives invitation to participate via web, LINE, CrewShip app, or paper.
  - Taps link or scans QR code.
  - Accesses the poll page in a browser on a smartphone or desktop.
  - Reviews the content and selects an A or B option.
  - Presses the Vote button.
  - Is directed to a “Thank You” page.
  - The “Thank You” page contains the current result of the poll (in percentages).
  - The “Thank You” page contains information about upcoming milestones, meetings, or opportunities to get more involved.

<p></p>

- **Web Content Manager** creates a poll:
  - Collects text and visual assets used in the poll.
  - Assembles the poll using a web template.
  - Publishes the poll on the website.
  - Tests the poll.
  - Resets the vote count of the poll to zero.
  - Creates invitations to take the poll on the city website, LINE, and CrewShip app.
  - Exports the invitation as a PDF with QR code.
  - Prints paper flyers and guides the distribution to locations.
  - Delivers the PDF or paper flyers for a mailing to all citizens.

<p></p>

- **City Official** reviews the results of a poll:
  - Digital: accesses the app and views the poll result page (...poll/result).
  - Analog: receives a report, via email or paper, with the poll result.
  - Archives the result to be used in a report or in decision making workflow.

## Architecture

Citizen Sentiment is intended to be deployed as an app within the Kesennuma city website. It could be accessible at a web address such as https://www.kesennuma.miyagi.jp/polls. It could also be a subdomain, such as https://polls.kesennuma.miyagi.jp/

### Features

- **Standard simple layout:** The poll has a limited set of page elements, including an eyebrow text, a heading with the title of the poll, a clarifying description text, two options marked A & B, selection indicators, a footnote, and a “Vote” button.
- **Page header:** The header of the poll page contains navigation and utilities. The exact header elements depend on the design of the parent website (the city website).
- **Link up to Polls:** One of the header elements is a link from the poll up to the Polls page.
- **Inherited design:** The polls section must follow the design rules of the city website.
- **Responsive design:** The poll pages are responsive, adjusting their layout according to the device being used to view the page.

- **Option panels:** The A/B option panels have several sub-elements: an image, an A or B label, a selection radio button, a caption, and an image expansion button. 
- **Image expansion function:** When images are used for the A/B choice, the images can be expanded by tapping on a double-arrow expansion icon. This allows users to closely inspect the image details.
- **Textual polls:** The poll can also be textual (with or without images), where a block of text is presented within the option panels. Textual polls can be used for proposed policy changes and such. 
- **Option selection:** When a user selects A or B, the option panel is highlighted with a dark border and a pulsing glow. Also a checkmark appears on the panel (see the demo site). 
- **Fixed vote button:** The “Vote” button is fixed to the bottom of the page so it is always in view. Users can scroll the content above the button.
- **Dynamic vote button:** When a user accesses the poll and hasn’t yet selected an A or B option, the vote button label reads “Choose A or B”. After the user has made a selection, the vote button label changes to “Vote for A” or “Vote for B”.
- **Multilingual user interface:** Polls are displayed in Japanese as the default language. A language switcher is available at the top right of the page with options for English, Indonesian, and perhaps others. If no translation is available the text stays in default Japanese.
- **Accessibility:** The poll pages must comply with "JIS X 8341-3: 2016", compliance level AA.

- **Mnemonic naming convention:** Polls must have a short and memorable file name, for instance https://www.kesennuma.miyagi.jp/polls/promenade. This enables citizens to verbally reference the poll. It is not practical to have a cryptic id for the poll name.
- **Poll result:** The result of a poll is available at ‘.../pollname/result’, e.g. https://www.kesennuma.miyagi.jp/polls/promenade/result. This makes it easy to view the result of any current or previous poll.

- **Polls page:** Poll users can navigate up to the Polls page, which lists all the polls that have been previously been conducted. The polls are listed in chronological order. If the amount of polls exceeds 10, the listing has batching.
- **:**
- **No authentication:**


### Technical Requirements
