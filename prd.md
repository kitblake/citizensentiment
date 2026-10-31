# Citizen Sentiment PRD v1

#### Metadata

Project:  Citizen Sentiment app  \
Conception: Built at the Kesennuma Hackatsuon, Sept 28 ~ Oct 10th 2026  \
Presented: October 10th, 2026  \
Presentation: https://docs.google.com/presentation/d/1MgNv7ET512Ok534cw667VMeXVcHkJLhF92t5bHKhpb8/edit?usp=sharing  \
Demo URL: https://citizen-sentiment-kesennuma.netlify.app/ja/poll  \
Demo PDF (paper flyer handed out at the presentation): Flyersetup.pdf  \
Github repo: https://github.com/kitblake/citizensentiment/  \
Source code: https://github.com/AkakpoErnest/HaboSavey/  \
Developer: Pablo Akakpo  \
PRD doc: https://github.com/kitblake/citizensentiment/blob/main/prd.md  \
Author: Kit Blake

## Abstract

Citizen Sentiment is a simple app that enables Kesennuma city officials to gather the preferences of citizens about a future project. It’s primarily visual where images, in A/B format, are distributed in multiple media, including web, app, and paper. Promotion includes a QR code link. After citizens scan the QR code they land on a poll page in the Citizen Sentiment app. They make a choice between image A and B and submit their preference. The city can then gauge the sentiment of the populace when making decisions.

### Intended Use

Citizen Sentiment is a tool for conducting polls within Kesennuma. The poll is distributed on the existing communication channels, including the Kesennuma city website, LINE, the CrewShip app, and as a paper flyer. The flyer can be placed at local restaurants and cafes and mailed to residents at their home address. In this way the city can be certain that the poll reaches most citizens and people concerned.

### Scope of this document

In the presentation Citizen Sentiment is described as an ‘app’. However, it’s not intended to be an application on a smartphone. The poll is meant to be a feature of the city website. It functions as an app within the website.

It’s also not the intention that the app in the website will be named Citizen Sentiment (or ). That’s simply the name of the project.

This document only describes requirements for the website implementation. Other channels, like LINE or the CrewShip app, can either direct residents to the poll page with a link, or integrate the poll into the platform. Those implementations need to be determined by the responsible administrators.

### Resources

### Roles

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
  - **Needs**: Access to poll results and analysis, ability to propose polls, access to the city communications team that is responsible for the website, LINE and CrewShip app.
  - **Pain points**: Difficulty learning how citizens feel about proposed changes within the city, limited access to online feedback tools, complex internet communication systems.

<!-- 4. **Community/Support Worker**
  - **Who they are**: City employee or freelancer responsible for interacting with citizens. The worker functions as both a liaison for the city and a support contact person.
  - **Needs**: Access to communication channels (telephone, chat apps, LINE, etc). Extensive FAQ database with answers to Frequently Asked Questions. Updates about planned campaigns that may trigger support requests.
  - **Pain points**: Difficulty helping elderly or non-tech savvy citizens navigate a smartphone or website, limited technical knowledge, language barriers, non-standard work times. -->


### User Stories

- As an **Ordinary Citizen**, I want to be informed about proposed changes in the city and share my opinion in a poll.
- As an **Ordinary Citizen**, I want to share my opinion effortlessly.
- As an **Ordinary Citizen**, I want to be informed about opportunities in the future to participate in a decision process.
- As an **Ordinary Citizen**, I want to learn how other residents feel about an issue.

<p></p>

- As a **Web Content Manager**, I want to efficiently create polls on the city website.
- As a **Web Content Manager**, I want to schedule polls with a start and end time.
- As a **Web Content Manager**, I want to create a QR code containing the website address of a poll.
- As a **Web Content Manager**, I want to create invitations to participate in a poll on the city’s communication channels.
- As a **Web Content Manager**, I want to create a PDF for a paper version of the invitation that can be distributed as a flyer.
- As a **Web Content Manager**, I want to manage an archive of polls that have been conducted and are publicly viewable on the website.
- As a **Web Content Manager**, I want to create multilingual polls.
- As a **Web Content Manager**, I want to create polls on the website that comply with "JIS X 8341-3: 2016", compliance level AA.

<p></p>

- As a **City Official**, I want to propose polls about important issues.
- As a **City Official**, I want to engage citizens in decision making processes.
- As a **City Official**, I want to make citizens feel like their opinions matter. 
- As a **City Official**, I want to make sharing opinions an effortless, enjoyable, and rewarding activity. 
- As a **City Official**, I want to learn how residents feel about a proposed project or policy. 
- As a **City Official**, I want to encourage citizens to play a more active role in change making processes. 
- As a **City Official**, I want to receive detailed feedback about the results of a poll.


### User Flows

