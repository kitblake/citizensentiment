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

Citizen Sentiment is a simple app that enables Kesennuma city officials to gather the preferences of citizens about a future project. It’s primarily visual where images, in A/B format, are distributed in multiple media, including web, app, and paper. Promotion includes a QR code link. After citizens scan the QR code they land on a poll page in the Citizen Sentiment app. They make a choice between image A or B and submit their preference. The city can then gauge the sentiment of the populace when making decisions.

### Intended Use

Citizen Sentiment is a tool for conducting polls within Kesennuma. The poll is distributed on the existing communication channels, including the Kesennuma city website, LINE, the CrewShip app, and as a paper flyer. The flyer can be placed at local cafes and venues and mailed to residents at their home address. In this way the city can be certain that the poll reaches most citizens and people concerned.

In the presentation Citizen Sentiment is described as an ‘app’. However, it’s not intended to be an application on a smartphone. The poll is meant to be a feature of the city website. It operates as an app within the website.

It’s also not the intention that the app will be named Citizen Sentiment (or 市民みんなの声). That’s only the name of the project.

### Scope of this document

This PRD only describes requirements for the website implementation. Other channels, like LINE or the CrewShip app, can either direct residents to the poll page with a link, or integrate the poll into the platform. Those implementations need to be determined by the responsible administrators.


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
- Citizen Sentiment is a low-barrier app. No login is required. The poll is anonymous and any individual can respond.
- By utilizing a QR code containing a web link, any citizen with a smartphone can easily scan the code and participate in the poll.
- The poll score (percentage of votes for choice A or B) is transparently shared with participants on the poll “Thank You” page.
- City officials can access a backend of the app with a more detailed breakdown of citizen participation and preferences.


## Users

### Target Audience

1. **Ordinary Citizens**
  - **Who they are**: Residents of Kesennuma city, or people who live elsewhere but work in the city.
  - **Needs**: Quick and easy access, clear guidance, immediate opportunity to share their opinion, voting task completion in 2 minutes.
  - **Pain points**: Complex interaction with existing services, difficulty with tech, unclear community resources, limited communication from the city/district.

2. **Web Content Manager**
  - **Who they are**: City employee or freelancer responsible for Content Management of the Kesennuma city website. Tasks include managing text and image assets used in polls, scheduling polls, and organizing poll distribution across media channels.
  - **Needs**: Efficient content management processes, automated technical integrations, ability to quickly update poll and communication material, relationships with other personnel involved in poll dissemination.
  - **Pain points**: Time-consuming manual processes, repetitive technical tasks, support issues, limited capacity for editorial contribution.

3. **City Officials**
  - **Who they are**: Elected officials and civil servants working in the city administration, city council members, and other positions serving as liaisons or as representatives of the populace.
  - **Needs**: Access to poll results and analysis, ability to propose polls, contact with the city communications team that is responsible for the website, LINE and CrewShip app.
  - **Pain points**: Difficulty learning how citizens feel about proposed changes within the city, complex internet communication systems, limited access to online feedback tools.

<!-- 4. **Community/Support Worker**
  - **Who they are**: City employee or freelancer responsible for interacting with citizens. The worker functions as both a liaison for the city and a support contact person.
  - **Needs**: Access to communication channels (telephone, chat apps, LINE, etc). Extensive FAQ database with answers to Frequently Asked Questions. Updates about planned campaigns that may trigger support requests.
  - **Pain points**: Difficulty helping elderly or non-tech savvy citizens navigate a smartphone or website, limited technical knowledge, language barriers, non-standard work times. -->


### User Stories

- As an **Ordinary Citizen**:
  - I want to be informed about proposed changes in the city and share my opinion in a poll.
  - I want to share my opinion effortlessly.
  - I want to be informed about opportunities in the future to participate in a decision process.
  - I want to learn how other residents feel about an issue.

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
  - I want to make citizens feel like their opinions matter.
  - I want to engage citizens in change making processes.
  - I want to learn how residents feel about a proposed project or policy.
  - I want to make sharing opinions an effortless, enjoyable, and rewarding activity.
  - I want to receive detailed feedback about the results of a poll.


### User Flows

- **Ordinary Citizen** participates in a poll:
  - Receives invitation to participate via web, LINE, CrewShip app, or paper.
  - Taps link or scans QR code.
  - Lands on the poll page in a browser on a smartphone or desktop.
  - Reviews the poll and selects an A or B option.
  - Presses the Vote button.
  - Is directed to a “Thank You” page.
    - The “Thank You” page contains the current result of the poll in percentages.
    - The page presents information about upcoming milestones, meetings, or opportunities to get more involved.

<p></p>

- **Web Content Manager** creates a poll:
  - Collects text and visual assets used in the poll.
  - Assembles the poll using a web template.
  - Assembles the poll “Thank you” page using a web template.
  - Tests the poll.
  - Resets the vote count of the poll to zero.
  - Publishes the poll on the website.
  - Creates invitations to engage with the poll on the website, LINE, and CrewShip app.
  - Exports the invitation as a PDF with QR code.
  - Prints paper flyers and guides the distribution to locations.
  - Delivers the PDF or paper flyers for a mailing to all citizens.

<p></p>

- **City Official** reviews the results of a poll:
  - Digital: accesses the app and views the poll result page (`...poll/result`).
  - Analog: receives a report, via email or paper, with the poll result.
  - Stores the result to be used in a report or in a decision making workflow.


## Architecture

Citizen Sentiment is intended to be deployed as an app within the Kesennuma city website. It could be accessible at a web address such as https://www.kesennuma.miyagi.jp/polls. It could also be a subdomain, such as https://polls.kesennuma.miyagi.jp/

### Features

- **Poll Elements**
  - **Standard simple layout:** The poll has a limited set of page elements, including an eyebrow text, a heading with the title of the poll, a clarifying description text, two options marked A & B, selection indicators, a footnote with the validity range, a footer with a link to the Privacy Policy, and a “Vote” button.
  - **Page header:** The header of the poll contains navigation and utilities. The exact header elements depend on the design of the parent website (the city website).
  - **Link up to Polls page:** One of the header elements is a link from the poll up to the Polls page (description below).
  - **Option panels:** The A/B option panels have several sub-elements: an image, a label with A or B, a selection radio button, a caption, and an image expansion button.
  - **Image expansion function:** When images are used for the A/B choice, the images can be expanded by tapping on a double-arrow expansion icon. This allows users to closely inspect the image details.
  - **Textual polls:** The poll can also be textual (with or without an image), where a block of text is presented within an option panel. Textual polls can be used for proposed policy changes and such.
  - **Option selection:** When a user selects A or B, the option panel is highlighted in multiple ways. The panel highlights with a dark border and a pulsing glow. A checkmark appears on the panel and the radio button fills as selected (see the demo site).
  - **Fixed vote button:** The “Vote” button is fixed to the bottom of the page so it is always in view. Users can scroll the content above the button.
  - **Dynamic vote button:** When a user accesses the poll and hasn’t yet selected an A or B option, the vote button is inactive and its label reads “Choose A or B”. After the user has made a selection, the vote button activates and its label changes to “Vote for A” or “Vote for B”.

<p></p>

- **App Characteristics**
  - **Inherited design:** The poll pages must follow the design rules of the city website.
  - **Responsive design:** The poll pages must be responsive, adjusting their layout according to the device used to view the page.
  - **Mnemonic naming convention:** Polls must have a short and memorable alphabetical file name, for instance https://www.kesennuma.miyagi.jp/polls/promenade. This enables citizens to verbally reference the poll. It is not practical to have a cryptic id for the poll name.
  - **Featured poll:** The featured poll is the newest open poll. It can be accessed at `.../poll` (what the demo flyer points to). This makes it easy to find the current poll. However invitations always link to the full poll name (e.g. `...polls/promenade`) to ensure the link will work in the future.
  - **Poll result:** The result of a poll is available at `.../pollname/result`, e.g. https://www.kesennuma.miyagi.jp/polls/promenade/result. This makes it easy to view the result of any current or previous poll.
  - **Polls page:** Poll users can navigate up to the Polls page, which is the index of `.../polls`. It lists all polls that are currently running and displays a list of previously conducted polls. Polls are listed in chronological order. If the amount of polls exceeds 20, the listing has batching.
  - **Viewing closed polls:** When viewing a previous poll the label of the Vote button becomes “View Result”. The button links to `...pollname/result`.
  - **No authentication:** When a user views a poll there is no login or authentication required. A citizen can vote immediately and anonymously. Both the poll and its result are publicly viewable.
  - **Accessibility:** The poll pages must comply with "JIS X 8341-3: 2016", compliance level AA.
  - **Privacy and Data Retention Policies:** A Privacy Policy and Data Retention Policy for the poll app need to be created. They should be published on the site and linked in the footer of each poll page.
  - **Multilingual user interface:** Polls are displayed in Japanese as the default language. A language switcher is available at the top right of the page with options for English, Indonesian, and perhaps others. If, after a language switch, no translation is available the text stays in default Japanese. If no translation at all is available then the language switcher should not display.

<p></p>

- **Backend Functionality**
  - **Content Management:** The Citizen Sentiment app will have a simple content management system for managing polls. This could be implemented in the system currently in use for the city website. It could also be a different, or custom, system. In both cases a more detailed PRD for the backend content management will need to be created.
  - **Poll lifecycle:** A poll has a workflow with states and transitions, proceeding from creation/editing, to publication, to running time, closure, and archiving. The backend has a moderation queue.
  - **Poll scheduling:** When a new poll is created it is configured with a start & end date. This determines when it becomes viewable and during what period citizens can engage with the poll.
  - **Poll archiving:** When a poll reaches its end date it automatically deactivates. The poll gets an archived state and is labeled accordingly in the Polls page listing.
  - **Poll retirement and deletion:** Polls that have been conducted can be retired, i.e. removed from public view. They can also be deleted for good.
  - **Detailed results:** The backend will display detailed results per poll, such as the total number of voters, the number who voted for A and B, and the percentages.
  - **Statistics:** The backend provides other insights into the poll statistics and usage, such as votes per day, votes per channel (each poster/newsletter/web QR code), plus CSV export (Excel-ready Japanese).

### Technical Requirements

As the infrastructure of the current Kesennuma City website is unknown, the following requirements are generic. To keep it simple, it’s assumed that the Citizen Sentiment app will be a custom implementation in its own environment like the [demo site](https://citizen-sentiment-kesennuma.netlify.app/ja/poll). See the [source code README](https://github.com/AkakpoErnest/HaboSavey/) for details and extensive technical docs.

- **Hosting:** The software for the app needs to run on a virtual server. For the demo we used Netlify hosting with static/SSR (Server Side Rendering) served via Netlify Edge. Other provider platforms are an option.
- **Code Deployment:** Whatever hosting situation is chosen, the instance should be integrated with the source code on Github to enable automated code deployment and builds.
- **Data Storage:** A Neon Postgres database is used for storing and retrieving the results of polls. Netlify's built-in database could also be used. It requires a paid account.
- **Localization:** If multilingual polls are desired then translation alone is insufficient. The content must have Localization (a.k.a ‘l10n’). In the demo site the Claude AI that built the app handled it. The demo site has ‘ja’ and ‘en’ prefixes in the path that are cross-linked, e.g. https://citizen-sentiment-kesennuma.netlify.app/ja/poll and https://citizen-sentiment-kesennuma.netlify.app/en/poll.
- **Fraud Prevention:** One of the risks of having an open and anonymous poll is fraudulent votes. A person or party might maliciously attempt to influence the poll result. The poll must have mechanisms that prevent multiple votes from a user or flood voting by bots.
  - **One vote per device:** The demo site has a simple mechanism to prevent double voting by citizens. However this solution is not viable in a production environment which has to contend with bots. More robust protection will need to be implemented.
  - **Anonymous Credentials:** In order to prevent fraud the poll could make use of Anonymous Rate-Limited Credentials. This is a [protocol developed at the IETF](https://www.ietf.org/archive/id/draft-privacypass-rate-limit-tokens-00.html).
  - **Anonymous Token-based Rate Limiting:** The easiest way to prevent fraudulent voting may be to use Cloudflare, which has a dedicated offering for per-user rate limits. This article describes [best practices](https://developers.cloudflare.com/waf/rate-limiting-rules/best-practices/).
- **About the Points in the demo site:** During the hackathon we decided to collaborate with another project and offer Points as an incentive. When citizens vote in a poll they receive Points as a reward. These points can be used in the [KesenMemento](https://github.com/ss251/kesenmemento-v2) game, implemented by [Jay Matsushiba]() and [Sailesh Sivakumar](). The Nickname feature in the demo site is only needed for the points. This PRD does not cover the Points features or additional game functionality present in the demo site. It focuses purely on the Poll aspects as presented on the October 10th Demo Day.


## Execution

### Milestones

- **MVP (2 Weeks):** Deploy initial poll app with full functionality; staff training; validate initial implementation with Kesennuma staff and volunteer testers.
- **Alpha (2-3 Weeks):** App testing with a local user group; comprehensive UI testing for improved user experience; iterative refinement.
- **Beta (4 Weeks):** Launch a public poll as a beta implementation; communicate with the Kesennuma community; share best practices among staff; collective troubleshooting; implement refinements.
- **1.0 version:** Operate polls over a six month period. Then review learnings, specify desired improvements, and schedule fixes.

### Success Metrics
- **Deploy 6 polls** with city-wide distribution of invitations over six months.
- **Onboard 10,000+ citizens** who engage with a poll.
- **Track via measurable engagement metrics** such as digital and paper invitations sent, polls accessed, polls completed, follow-up actions taken.

### Risks and Challenges

- **Infrastructure Cost:** Ensuring reliable hosting without excessive costs.
- **Operational Costs:** Streamlining man-hour needs for poll operations, ensuring efficient distribution for digital and paper invitations.
- **Data Privacy:** Maintaining strict compliance with global and local privacy standards. Informing users about how their data is being processed.
- **Competition from Existing Tools:** Clearly articulating value propositions unique to Kesennuma.
- **User Adoption and Retention:** Continuously enhancing and simplifying UX/UI to reduce barriers.
- **Security Vulnerabilities:** Monitoring, conducting regular audits, and maintaining transparent security practices.


## Conclusion

Citizen Sentiment is a deliberately small, low-friction tool with an outsized civic purpose: it converts passive residents into participants by reducing "sharing an opinion" to a two-minute A/B choice. It reaches citizens through channels Kesennuma already uses: the city website, LINE, CrewShip app, and paper flyers distributed with a QR code. By returning immediate value through transparent results on the Thank You page, the design directly attacks the core problem identified in the Rationale: citizens feeling uninvolved.

The PRD scope is focused, specifying only the website implementation and deferring channel integrations and backend CMS details to follow-up work. Requirements remain concrete enough to build against, including JIS X 8341-3:2016 AA accessibility, multilingual support, mnemonic poll URLs, a defined poll lifecycle, and fraud prevention for anonymous voting. Success hinges less on technology than on operational execution. Delivering six city-wide polls and ten thousand engaged citizens over six months would prove a repeatable pattern for municipal consultation, giving residents who never attend a meeting an effortless way to be counted.

--
