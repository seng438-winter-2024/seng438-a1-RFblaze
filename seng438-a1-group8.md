>   **SENG 438 - Software Testing, Reliability, and Quality**

**Lab. Report \#1 – Introduction to Testing and Defect Tracking**

| Group: 8      |
|-----------------|
| Beljic, Stevan                |   
| Brahmbhatt, Rutvi              |   
| Giang, Aaron               |   
| Troncone, Angelo                |   


**Table of Contents**

(When you finish writing, update the following list using right click, then
“Update Field”)

[1 Introduction	1](#_Toc439194677)

[2 High-level description of the exploratory testing plan](#_Toc439194678)

[3 Comparison of exploratory and manual functional testing](#_Toc439194679)

[4 Notes and discussion of the peer reviews of defect reports](#_Toc439194680)

[5 How the pair testing was managed and team work/effort was
divided](#_Toc439194681)

[6 Difficulties encountered, challenges overcome, and lessons
learned](#_Toc439194682)

[7 Comments/feedback on the lab and lab document itself](#_Toc439194683)

# Introduction

The purpose of the lab is to go through the 4 main sections:

- Familiarizing ourselves with the system under test and defect tracking system  
- Exploratory testing  
- Manual scripted testing  
- Regression testing (upon different versions of the SUT)
  
Firstly, we familiarize ourselves with the system (ATM simulation) as well as the defect tracking system. Afterwards comes exploratory testing in which we can test the system in whichever way we deem fit. Manual scripted testing follows, where we perform tests on the SUT following a predefined test suite. Finally, we perform regression testing by testing the new udpdated version of the ATM simulator and then compare the differing system behaviour and document it in the defect tracking system.  
  
We had fairly little formal, applied knowledge and experience of testing and its various methods before this lab. We have had some experience in exploratory and regression testing, however it was fairly informal and we did not perform defect tracking in a disciplined manner.

# High-level description of the exploratory testing plan

### Stevan & Rutvi

Our exploratory testing plan is to simulate the interactions of users with the ATM system V1.0 in the 4 main task flows: deposits, withdrawls, transfers, and balance inquiries, as outlined in Appendix B. We believe this plan is a good blend between freely exploring the SUT while also following a plan to at least cover the main functions/uses for the average user of the system.


While the inputs for each execution of a task-flow will be random, the actions taken (buttons clicked, user-flow executed) are not as we delibaretly wish to extensively test each of the main user-flows. Each of us will perform 2 executions of each user flow (8 total executions per person, 16 total in pair), giving us a deep look into the functionality of the SUT and helping us find any glaring issues quite easily. Our primary desire with this in-depth exploratory testing plan is to cover a wide range of potential user inputs, such as the amount of moving in/out the system or the account being accessed, through random inputs while strictly following the user task flows and ensuring all main user functions can be accomplished, or at least understand wherein the issues lie.


Our plan is to have one of us perform (the executor) the task flow, while the other (the recorder) documents all user inputs and ensuring the executor is adhereing to the initially outlined plan. The recorder will also note any irregularities/abnormalities to the percieved output of the system, and will note the location, actual output, and expected output of the error. Upon two completions of each task flow, we will swap roles.

### Aaron & Angelo

For our exploratory testing, we decided to begin by briefly laying out every aspect and function of the program that was described in the lab document and ranked each based on levels of severity and fault tolerance. This allowed us to get a brief idea about how much we should test each function.


We then began testing the 4 main transactions of the ATM System Version 1.0 by providing a valid credit card number and PIN, and valid values. This was to familiarize ourselves with the system before beginning more extensive testing. We unexpectedly noticed a few minor bugs; bugs that were the most likely to be discovered through regular use. We used plausible values and abstained from trying to use boundary values and doing robustness testing, thus, allowing us to immediately identify flaws in functionality without much time and effort being invested.


Our main goal wasn't necesarily to find bugs at this point, but just understand the system were supposed to analyze. Once we understood the functionality of the program, and found bugs through our mundane use with reasonable values, we began to test boundary values and trying to break the program. This was when we started to find edge cases and uncommon bugs that wouldn't normally be discovered. We each were testing independently and reported back to each other what we found. We logged our findings in a shared text document as we were not familiar with Jira or Azure DevOps at the time we started exploratory testing.


# Comparison of exploratory and manual functional testing

Exploratory testing was conducted in two pairs and was done in an unscripted manner. A general testing plan was made by each pair to determine how to proceed through testing the software, however no strict script was followed. Tests were generally conducted by just interacting with the software and trying out various inputs within the confines of the general testing plan.

Comparatively, the manual scripted testing was much more rigid in execution and had specific steps which had to be undertaken. Manual scripted testing involves following a script of test cases to provide the software specific inputs and task-flows, and then examining the output of the system on those test cases compared to the expectd output.

We found the benefits of exploratory testing to be:
- Provides a greater range of data on system behaviour on slightly varied inputs
- Develops greater understanding of the function of the SUT
- Less rigid nature allows for more creative test cases
- Allowed for quicker discovery of bugs as documentation was only necessary when something abnormal happened

We found the benefits of manual scripted testing to be:
- Better suited for regression testing as tests could be easily replicated
- Bugs are more easily reproduced as steps to generate each bug are explicitly outlined in the script

While we found both methods to be very useful in uncovering bugs in the system, we found exploratory testing to overall be more effective and useful in uncovering bugs. Not only did exploratory testing help us to further understand the inner-workings of the SUT, but it also lead to more creative test cases in which we tried out various inputs to see what worked and what didn't. A lot of the bugs produced in manual scripted testing had already been discovered through exploratory testing. Still, it was beneficial to undertake both test methods as manual scripted testing improved our documentation and the reproducibility of previously discovered bugs.

# Notes and discussion of the peer reviews of defect reports

Our team ensured that all key elements in bug reports were included, such as the function being tested, initial system state, detailed steps to reproduce, and expected versus actual outcomes.
Our exploratory test plan was well-documented, covering all major targeted functions of version 1.0, testing approach with pairing up in a team, and paths to be explored.
Defects were recorded promptly during exploratory testing by both the pairs having detailed conditions were combined.
We played as a team during manual scripted testing, with one student driving, the other one tracking tests and the rest two, reporting defects and maintaining the document.
The division of defects for retesting in the regression phase (10 for each)  was well-coordinated among team members.
We concluded the result by reviewing our defects report that, out of 5 major bugs that were detected during manual scripted testing, 2 got resolved by doing regression testing.



# How the pair testing was managed and team work/effort was divided 
### Pair Testing

To conduct pair testing, we split ourselves up into two even pairs:
- Stevan & Rutvi
- Aaron & Angelo

Each pair had its own method of pair testing, but we followed the same principle as outlined in the assignment description, in which the executor would run exploratory tests on the software while the recorder would document the results in a document (wherefrom the data was input into Devops later). After an ample number of tests/use-cases were covered, we swapped roles and performed slightly different tests.

### Manual Scripted Testing

Manual scripted testing was performed together as a group. We met up in a workroom and had Angelo share his screen while one of us guided him though the tests, and the other would record the results of the tests in a shared document. After finishing up the testing and initial recording, we input the recorded data into a Devops project. After we performed all fourty test cases together and then divided them up into four even groupings and assigned them to each person to perform regression testing. After we performed our regression testing, we each updated the work items assigned to use in Devops to reflect the new behvaiour of the test cases in version 1.1 of the ATM.

# Difficulties encountered, challenges overcome, and lessons learned

Some difficulties we encountered during the lab were:

- We were unsure if some thing were bugs, or intended design. Things such as some of the messages displayed from rejected money transfers, or not having Savings listed in the Balance Inquiry, we were not able to distinguish whether they were intentional designs or bugs.
- Learning how to use Azure Devops & Jira. Initially we tried to use Jira, but found Devops to be more intuitive and simple so we proceeded in Devops. Even still, we found it difficult to initially learn how to report bugs while properly recording the version of the program it was associated with, and even initially setting up the project.

Some of the lessons we learned were:

- How to effectively write bug reports within a project reporting system. This includes learning what to record (steps to reproduce, expected vs. actual outcomes) and how to record (using the system itself, recording the project version)
- How to conduct exploratory testing, manual scripted testing, and regression testing

# Comments/feedback on the lab and lab document itself

### Stevan

The lab was a good introduction to the disciplined process of testing (and the multiple methods it may take on) and how to properly report bugs within a bug-tracking system. The processes of exploratory testing, manual scripted testing, and regression testing were simple enough to understand and perform on the ATM system. The largest challenge with this lab was learning how to effectively use the bug-tracking system (Azure Devops), a few better resources would've been helpful. There was a significant learning curve to learning how to use the platform. Furthermore, the requirments of the lab report were somewhat vague and it was challenging to understand what to write about in each section of the report. The process of testing itself was well-outlined and described, and we did not have issues conducting and recording tests.

### Rutvi

The key elements for bug reports are well articulated in the lab document, covering essential aspects such as the function being tested, initial system state, steps to reproduce, expected and actual outcomes.
The recommendation to create a high-level exploratory test plan is excellent. It encourages thoughtful testing and planning, promoting efficiency.
The usage of a basic test suites of Manual scripted testing in Appendix C adds structure to the testing process. Executing each test case at least once ensures comprehensive coverage.
The emphasis on updating defect status and commenting on the status change in Regression testing provides transparency and clarity in tracking defect resolutions.
Overall, the lab offers a methodical and organized way to acquire efficient approaches for reporting bugs and conducting tests.

### Aaron

The lab was very helpful in learning exploratory, manual scripted, and regression testing. Having a simulation program like the ATM system was a practical environment to apply these testing methods. The pair programming for the exploratory testing was effective in finding a wide range of scenarios and bugs. The manual scripted testing was nice to go through the program and test each feature individually systematically. Learning how to use Azure DevOps was one of the challenges but will be useful when we enter the industry. I found the Instructions were mostly clear and straightforward.

### Angelo

The lab provides a good introduction to exploratory, manual scripted, and regression testing, aswell as good practical experience to apply these techniques. It also showcased the strengths and weaknesses of the different types of testing, through which bugs were purposefully included in the SUT; some being only able to discovered during exploratory testing because there were no test cases that dealt with them. The Test Suite and SUTs being provided was very helpful, as it enabled us to only focus on learning about testing and not get sidetracked with programing. One criticism I have about the lab document was that I found the definition of exploratory testing a bit unclear as to how it is different to manual scripted testing. I would have liked to get more clear definitions and expectations when it came to that part of the lab. Overall, the lab instructions and expectations were easy to understand.
