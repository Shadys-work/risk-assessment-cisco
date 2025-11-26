  <h1>Risk Assessment for Cisco (informal)</h1>

  This document is more of an informal document that would document every step I've preformed, my thought process, how I've reached to conclusions, personal key findings and personal suggestions. You would read this documents if you want to find how I've come to a specific conclusion and what I personally think about certain aspects of this risk assessment and cisco. Reminder, this is not a personal project, it is a project from my university that requires me to match and fill the requirements my professor asks from me. 

  <h3> Selecting Cisco </h3>
  In all honesty, my intial organization was going to be cloudflare because I have read their documents before and I liked how techincal they get within their own infastructure, but unfortunately that idea was taken before I could take it. So I decided on Cisco, having dealt with Cisco's provided courses in my university (in my course Internet of Things) and having used their Cisco packet tracer to build networks for my "Introduction to network" and "Internet of Things" programs, I chose Cisco with some confidence (Not knowing what I was going to get myself into)

Why Cisco?
1. Have some familiarity with their applications
2. Knowledge of their background as a globally leading network service
3. Confidence that such a company would have a few open source information I could work with
  
<h2>Phase 1: Advanced Threat Modeling</h2>
The first phase of this project is to model my threat factors with STRIDE and DREAD. To do so, we first have to go through a few things in order to write a proper assessment with STRIDE and DREAD.

<h3>Multi-Layered Data Flow Analysis</h3>
For any feasible, meaningful threat modelling, we first require 2 things: Context and Asset. Both are important factors for constructing a threat model since we need A. A context that lets me know who am I dealing with exactly? what are the organization's priority? What brings in the most amount of revenue? and B. What are the assets I'll preform the both STRIDE and DREAD scoring on? Why would I choose this asset? Is this asset a crucial component in their operations and revenue? 
To do so, I am required to build 2 types of DFDs: A Business Logic DFD and Technical architecture DFD. Both containing trust boundaries where data crosses different security domains.

<h4>Business Logic DFD</h4>
This DFD wasn't so hard to build, I mainly thought about what components would make up the business operation and what goes on between the user and Cisco when a transaction over a service or product is made. The PDF for the business logic is in the report.pdf.
