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
<h4>Technical Architecture DFD</h4>
This one was a challenge, since I am not assessing Cisco's web application, but Cisco as a whole, I had to assess their products and services which meant I had to carefully pick out which services would help build a good foundation as we go deeper on them later in the project. The problem is Cisco has so many products and services, partnerships and supply chains. This proved to be challenging since I had to read up on their products and find a few things: 1. whether or not this asset is worth assessing (not a crucial component in their revenue stream) 2. Has a history of risks or attacks preformed on it otherwise it would be difficult to calculate the loss potential for the said asset 3. I could understand and draw out what the inner workings of the said asset. The hardest of them was point 3, since that required me to go through many of the documents posted up on their website to understand on a techincal level how does data flow between the service/product they provide. Point 1 was easy to find, a quick search told that their highest earning assets were selling software and hardware products. IoT is still making its way through. Point 2 was also quite simple, they have a security advisoer page up where they record all the past vulnerabilites and their ratings, including the numerous articles released and CVE's recorded for Cisco's systems.
For now, I have chosen their Cisco catalyst service and their Cisco IOS and IOS XE product line for more in-depth. At the time of writing this, there were many attacks preformed on both subjects. Since these are deployable products, there isn't a single model that abides in all infastructure, that meant I had to build a general technical architecture DFD using these deployable services/product but for me to do that, I had to first research on what Cisco catalyst and Cisco IOS were and how were they used. With the the help of ChatGPT, I am then able to build a sample of what a DFD level 1 would look like for either. 
<h5> Cisco Catalyst </h5>
At the time of reading the Cisco's DNA center and Catalyst, It was quite smart the idea Cisco had in mind. The issue they tackled using Cisco Catalyst is an identity and policy issue. Since every device is assigned a vlan to the physical area they are in, which means every place has its own policies and what the device has access to, its hard to transmit data or preform actions in other in real life places where such policies don't exist or are restrictive. Catalyst solves this by assigning the device its own seperate identity aside from its location using Locator/ID Separation Protocol (LISP). This allowed the user to be bounded by the policies implenented on their identity instead of their location.

<h5>Cisco IOS</h5>

