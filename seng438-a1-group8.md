>   **SENG 438 - Software Testing, Reliability, and Quality**

**Lab. Report \#1 – Introduction to Testing and Defect Tracking**

| Group: Group Number      |
|-----------------|
| Beljic, Stevan                |   
| Brahmbhatt, Rutvi              |   
| Giang, Aaron               |   
| Troncone, Angelo                |   


**Table of Contents**

(When you finish writing, update the following list using right click, then
“Update Field”)

[1 Introduction	1](#_Toc439194677)

[2 High-level description of the exploratory testing plan	1](#_Toc439194678)

[3 Comparison of exploratory and manual functional testing	1](#_Toc439194679)

[4 Notes and discussion of the peer reviews of defect reports	1](#_Toc439194680)

[5 How the pair testing was managed and team work/effort was
divided	1](#_Toc439194681)

[6 Difficulties encountered, challenges overcome, and lessons
learned	1](#_Toc439194682)

[7 Comments/feedback on the lab and lab document itself	1](#_Toc439194683)

# Introduction

The purpose of the lab is to go through the 4 main sections:

- Familiarizing ourselves with the system under test and defect tracking system  
- Exploratory testing  
- Manual scripted testing  
- Regression testing (upon different versions of the SUT)
  
Firstly, we familiarize ourselves with the system (ATM simulation) as well as the defect tracking system. Afterwards comes exploratory testing in which we can test the system in whichever way we deem fit. Manual scripted testing follows, where we perform tests on the SUT following a predefined test suite. Finally, we perform regression testing by testing the new udpdated version of the ATM simulator and then compare the differing system behaviour and document it in the defect tracking system.  
  
We had fairly little formal, applied knowledge and experience of testing and its various methods before this lab. We have had some experience in exploratory and regression testing, however it was fairly informal and we did not perform defect tracking in a disciplined manner.

# High-level description of the exploratory testing plan

**Stevan & Rutvi**

Our exploratory testing plan is to simulate the interactions of users with the ATM system V1.0 in the 4 main task flows: deposits, withdrawls, transfers, and balance inquiries, as outlined in Appendix B. We believe this plan is a good blend between freely exploring the SUT while also following a plan to at least cover the main functions/uses for the average user of the system.


While the inputs for each execution of a task-flow will be random, the actions taken (buttons clicked, user-flow executed) are not as we delibaretly wish to extensively test each of the main user-flows. Each of us will perform 2 executions of each user flow (8 total executions per person, 16 total in pair), giving us a deep look into the functionality of the SUT and helping us find any glaring issues quite easily. Our primary desire with this in-depth exploratory testing plan is to cover a wide range of potential user inputs, such as the amount of moving in/out the system or the account being accessed, through random inputs while strictly following the user task flows and ensuring all main user functions can be accomplished, or at least understand wherein the issues lie.


Our plan is to have one of us perform (the executor) the task flow, while the other (the recorder) documents all user inputs and ensuring the executor is adhereing to the initially outlined plan. The recorder will also note any irregularities/abnormalities to the percieved output of the system, and will note the location, actual output, and expected output of the error. Upon two completions of each task flow, we will swap roles.

**Aaron & Angelo**

For our exploratory testing, we first began testing the 4 main transactions of the ATM System Version 1.0 by providing a valid credit card number and PIN, and valid values. This was to familiarize ourselves before doing more extensive testing. We unexpectedly noticed a few minor bugs, and bugs that were the most likely to be discovered through regular use. Our main goal wasn't necesarily to find bugs at this point, but just understand the system were supposed to analyze. Once we understood the functionality of the program, we then began to test boundary values and trying to break the program. This was when we started to find edge cases and uncommon bugs that wouldn't normally be discovered. We each were testing independently and reported back to each other what we found.


# Comparison of exploratory and manual functional testing



# Notes and discussion of the peer reviews of defect reports

Text…

# How the pair testing was managed and team work/effort was divided 
**Pair Testing**

To conduct pair testing, we split ourselves up into two even pairs:
- Stevan & Rutvi
- Aaron & Angelo

Each pair had its own method of pair testing, but we followed the same principle as outlined in the assignment description, in which the executor would run exploratory tests on the software while the recorder would document the results in a document (wherefrom the data was input into Devops later). After an ample number of tests/use-cases were covered, we swapped roles and performed slightly different tests.

**Manual Scripted Testing**

Manual scripted testing was performed together as a group. We met up in a workroom and had Angelo share his screen while one of us guided him though the tests, and the other would record the results of the tests in a shared document. After finishing up the testing and initial recording, we input the recorded data into a Devops project. After we performed all fourty test cases together and then divided them up into four even groupings and assigned them to each person to perform regression testing. After we performed our regression testing, we each updated the work items assigned to use in Devops to reflect the new behvaiour of the test cases in version 1.1 of the ATM.

# Difficulties encountered, challenges overcome, and lessons learned

Some difficulties we encountered during the lab were:

- We were unsure if some thing were bugs, or intended design. Things such as some of the messages displayed from rejected money transfers, or not having Savings listed in the Balance Inquiry, we were not able to distinguish whether they were intentional designs or bugs.
- Learning how to use Azure Devops & Jira. Initially we tried to use Jira, but found Devops to be more intuitive and simple so we proceeded in Devops. Even still, we found it difficult to initially learn how to report bugs while properly recording the version of the program it was associated with, and even initially setting up the project.

Some of the lessons we learned were:

- How to effectively write bug reports within a project reporting system. This includes learning what to record (steps to reproduce, expected vs. actual outcomes) and how to record (using the system itself, recording the project version)
- How to conduct exploratory testing, manual scripted testing, and regression testing

# Comments/feedback on the lab and lab document itself

**Stevan**

The lab was a good introduction to the disciplined process of testing (and the multiple methods it may take on) and how to properly report bugs within a bug-tracking system. The processes of exploratory testing, manual scripted testing, and regression testing were simple enough to understand and perform on the ATM system. The largest challenge with this lab was learning how to effectively use the bug-tracking system (Azure Devops), a few better resources would've been helpful. There was a significant learning curve to learning how to use the platform. Furthermore, the requirments of the lab report were somewhat vague and it was challenging to understand what to write about in each section of the report. The process of testing itself was well-outlined and described, and we did not have issues conducting and recording tests.

**Rutvi**

**Aaron**

**Angelo**
