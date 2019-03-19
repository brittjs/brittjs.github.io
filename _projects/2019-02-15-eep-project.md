---
title: 'European Energy Pilot'
subtitle: 'UX Design'
date: 2018-02-15 00:00:00
description: Using BTL’s blockchain platform, BTL, BP, Eni, and Wien Energie undertook a twelve-week pilot to design and develop a blockchain-based product that could achieve trade-by-trade reconciliation. 
featured_image: '/images/eep/eep-cover.png'
---

## Context
When trading energy products, issues with record keeping and data management can lead to costly errors and wasted time. These errors are caused by trade data being sent as PDF attachments via email, manual entry of data into gas balancing and portfolio management software, unaccounted for trade updates that lead to data discrepancies among counterparties, and manual searches through filed PDFs to find the latest trade updates. In addition, reconciling the amount of product that was sent versus what was actually received, can lead to delays for invoicing.

## Problem
Data discrepancies occur when counterparties don't share a central place to input, store, and keep a record of trade information and updates. Spending the time and resources to pursue all losses caused by such discrepancies would not be practical, so losses below a certain value (often in the thousands) are  not pursued. As one can imagine, these errors add up and can lead to losses of hundreds of thousands, even millions of dollars.

## Solution
Using BTL’s blockchain platform, BTL, BP, Eni, and Wien Energie undertook a twelve-week pilot to design and develop a blockchain-based product that could achieve trade-by-trade reconciliation more efficiently with less errors compared to current processes by providing a central place for traders to create, modify/update trade data (while also keeping a record of all previously submitted transaction reports), automating the matching of trades entered by counterparties, and defining a business process for reconciliation.

The project team understood that blockchain technology’s applicability extends across the range of back office processes (reconciliation, actualization, invoicing, netting), and is not limited to trade-by-trade reconciliation. This pilot was undertaken as a first step in demonstrating how blockchain technology can reshape processes throughout the entire back office.

## My Role
UX design. I was responsible for creating the interactive wireframes that were used to demonstrate the user stories as well as creating medium fidelity mockups.

## Tools

Balsamiq (interactive wireframes/prototype), Photoshop (medium fidelity mockups)

## Process

All three participating energy companies were directly involved in co-creating a potential solution that would benefit all parties. This collaborative approach was chosen recognizing that each of the participants face similar risks and challenges in back office processing, despite any variations that may exist in scale and commodities traded. At the beginning of the pilot, a kickoff meeting, regular collaborative meetings, and individual sessions were planned to gather functional requirements, identify data to be used, confirm user stories to be tested, and answer key questions about technology, security, privacy, and scalability.

## Interactive Wireframes & Mockups

I worked collaboratively with BTL’s CTO, CIO, Project Manager, and the Head of Product Enablement to complete the interactive wireframes for a real-time reconciliation dashboard. The interactive wireframes were used to demonstrate the eight user stories created for the pilot. Before I get into the user stories, I will first provide some information on the dashboard.

#### Dashboard

![](/images/eep/user_story_1_slide_1.png)

The application featured four tabs.

**THE REPORTS TAB -** This was the primary tab that showed all trades relevant to the counterparty and displayed the most important information for each trade:   
a) the timestamp for when the trade was entered into the system,  
b) the UTI ("unique trade identifier"),  
c) the other counterparty involved in the trade,  
d) the public key used to access the distinct blockchain shared between the two counterparties,  
e) the asset being _sent_ (an energy product or amount of money),  
f) the asset being _received_ (an energy product or amount of money),  
g) the direction the last trade report was sent (inbound indicates you need to take action, outgoing indicates you're awaiting action from the other counterparty), and  
h) the status of the transaction report. This tab was the most important of the pilot and I'll provide more details after briefly explaining the next three tabs.

**THE BATCH UPLOAD TAB -** This tab contains a file selector to allow a user to upload a batch of existing transaction reports to display in the reports tab. This feature was not required for completion, but was included to show a way for existing transaction reports to be entered into the system.

**THE DIRECTORY TAB -** This tab contains information on each of the counterparties the user has a trade chain with. This feature was not required for completion.

**THE BLOCK EXPLORER TAB -** This tab was not part of the product, but was used to showcase what was happening under the hood. Each time a report was created or modified, you could see the changes added to the blockchain. This feature was not required for completion.

#### Details on the Reports Tab

Colour was used as a way for the user to scan the trade statuses and to quickly see which needed attention.

| Colour   | Status       | Meaning                                           |
|----------|--------------|---------------------------------------------------|
| Green    | Confirmed    | Both parties have agreed on the trade data        |
| Yellow   | Pending      | Only one party has submitted a transaction report |
| Red      | Disputed     | Data doesn't match between the counterparties' transaction reports |

There are four different buttons on the Reports tab. Aside from the "Create" button, the other three buttons allow the user to perform an action on the selected transaction report. We decided to place these buttons at the top so that the user could easily see the actions that could be performed, and to avoid adding another column to the table of reports. If no report is selected, then the "Review", "Delete", and "Explore" buttons are disabled. 

| Button   | Function                                            |
|----------|----------------------------------------------------|
| Create   | Opens a modal to create a new transaction report   |
| Review   | Opens a modal to review and/or update the selected report and its history |
| Delete   | Opens a modal asking the user to confirm deletion. This action can only be taken on an outgoing pending transaction report   |
| Explore  | Opens the block explorer to the selected transaction |

The "Review Transaction Report" modal has a section on the left where a user can input their version of the trade data. The right side displays all previously submitted versions of the transaction report. We chose to do a horizontal scroll for submitted trade reports so that we could compare the reports side by side, and draw attention to the differences between: a) the two most recent submitted reports, and/or  the data the user is currently entering compared to the last submitted report.

#### User Stories

Here are 5 of the 8 user stories.

<div class="gallery user-story" data-columns="2">
  <img src="/images/eep/user_story_1_slide_1.png">
  <img src="/images/eep/user_story_1_slide_2.png">
</div>
**Simple Trade Match:** Demonstrating that trades with identical unique trade identifiers (UTIs) and attributes could be matched on the platform with the appropriate status shown on the dashboard.

---

<div class="gallery user-story" data-columns="3">
  <img src="/images/eep/user_story_2_a-c_slide_1.png">
  <img src="/images/eep/user_story_2_a-c_slide_2.png">
  <img src="/images/eep/user_story_2_a-c_slide_3.png">
</div>
**A ‘Hanging’ Trade:** Demonstrating that a trade that has been entered by only one party can be shown as _pending_ on the dashboard, and that the status is updated to _matched_ when the other party to the trade updates their side.

---

<div class="gallery user-story" data-columns="3">
  <img src="/images/eep/user_story_3_slide_1.png">
  <img src="/images/eep/user_story_3_slide_2.png">
  <img src="/images/eep/user_story_3_slide_3.png">
</div>

**A Simple Mismatch - Amendment before Matching:** Demonstrating that two trades that match on UTI, but have an unmatched attribute, will maintain a _disputed_ status until the appropriate party to the trade alters and updates the disputed attribute, creating a match.

---

<div class="gallery user-story" data-columns="2">
  <img src="/images/eep/user_story_4_slide_1.png">
  <img src="/images/eep/user_story_4_slide_2.png">
</div>

**A Complex Mismatch - Amendment before Matching requiring Communication and Multiple Amendments to Resolve:** Demonstrating (1) that two trades that match on UTI, but have multiple unmatched attributes, will maintain a disputed status until the appropriate party to the trade alters and updates the disputed attribute(s), and (2) that communication to resolve the dispute regarding the attribute(s) is possible via the blockchain rather than email, and that these messages can be exchanged multiple times until the dispute is resolved creating a match.

---

<div class="gallery user-story" data-columns="3">
  <img src="/images/eep/user_story_5a_slide_1.png">
  <img src="/images/eep/user_story_5a_slide_2.png">
  <img src="/images/eep/user_story_5a_slide_3.png">
</div>

**Matched Trade is Unmatched and can be Rematched - Economic Amendment after Matching:** Demonstrating that a previously matched trade can be unmatched, attribute(s) can be disputed and resolved, and can result in a recreated match.

---

During the weekly meetings with the participants, the interactive wireframes were presented and feedback was gathered. After a few weeks of iteration, the participants were satisfied and the next step was to create medium fidelity mockups.

<div class="gallery" data-columns="2">
  <img src="/images/eep/mock_reports.png">
  <img src="/images/eep/mock_create_txn_report.png">
</div>

All design materials were then handed over to the developer to be built.

![](/images/eep/reports.png)

## User Story Testing

All participating energy companies were given access to the application. During the execution of the user stories, the participants had the opportunity to access and test the platform’s functions, both with BTL and independently. The pilot application was successful in demonstrating all eight user stories.

<div class="gallery" data-columns="2">
  <img src="/images/eep/UserStories1.png">
  <img src="/images/eep/UserStories2.png">
</div>

## Outcome

The pilot successfully demonstrated that reconciliation could be executed on a trade-by-trade basis using blockchain. This outcome provided evidence for the broader, transformative potential that blockchain technology promises to deliver across the range of back office activities that support trading operations within energy companies.

The success of the pilot led to OneOffice - the second phase of BTL’s European energy project, which included participants like Eni Trading & Shipping, Total, Gazprom Marketing & Trading Limited, Mercuria, Vattenfall, Petroineos and Freepoint to deliver cost savings across the trade life cycle.

## Key Learnings

The 100% utilitarian look for this pilot application was intentional. The priority of this project was to produce a functional application that could demonstrate the value that BTL’s blockchain platform could bring to back office processing. Having an aesthetically pleasing UI was a stretch goal.

After the stakeholders were satisfied with the interactive wireframes, I quickly created three very basic themed sets of mockups for the CIO to choose from. This project had a timeline of twelve weeks with one developer assigned to the project. When looking back and focusing on functionality as the priority, I should have created a single set of mockups so that the handover to the developer would have occurred sooner. While it's important to have a design process you would normally adhere to, it is also important to be selective and to know which parts can be omitted, especially when working within a shorter time frame.