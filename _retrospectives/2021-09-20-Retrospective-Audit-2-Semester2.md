---
layout: post
tag:
  - "Audit"
  - "Retrospective"
---

> Our team members have been focusing on the implementations of a Customer Portal and a Local Order Management System for ANFF OptoFab ACT since the last audit.

{% include toc %}

## Details

### Audit 2

|               | Information                                                                       |
| ------------- | --------------------------------------------------------------------------------- |
| Date and time | 01/09/2021 17:00-19:00                                                            |
| Participants  | @Phillip Wu @Wo Tian @Ruiqiao Jiang @Ruoqian Wu @Yaoyi Xu @Hengrui Xu @Guoyu Wang |
| Tutor         | Greg Bek                                                                          |
| Examiner      | Priscilla Kan John                                                                |

### Tag Reports

Team members and stakeholders complete the tag reports before the teaching break to provide and respond to constructive feedback according to the [evaluation process](https://cs.anu.edu.au/TechLauncher/current_students/evaluation/tag_reports/).

## Rubrics

Refer to: <https://cs.anu.edu.au/TechLauncher/current_students/evaluation/project_audits/ >

## Feedback

The feedback is mainly based on the tag reports from the TechLauncher Feedback Portal.

### Project Output

**Good**

Client is positive in the output of the team as both sides of the project are progressing.

**Bad**

1. [Issue 1 (I1 for short)]Client: The team "should be careful not to over-invest in one part of the project if it means taking away from a different part. Not a problem at the moment, but a potential pitfall in the future."
2. [I2]Tutor: "...there is wide variance across the team in some weeks - 7 hours to 14+ hours."
3. [I3]Tutor: "The entity relationship diagram give the appearance of being over complicated. There are many instances of small data types being represented with an ID (used else where as a foreign key) and a single character value, with cardinality ommmited on the relationships. There seems little point in factoring out to separate table if a 1:1 relationship is used in these cases."
4. [I4]Shadow: "We understand that there are 2 spokesperson in the team hence 2 people in charge of communication. However, that does imply that the other members in the team are not communicating at all (in the teamwork slide)."

**How to improve**

1. [I1] Portal vs Database. Many database fragements depend on the exported files from out website portals, so we have to focus more and "over-invest" a little bit in the portal side. Now it's nearly finished on the portal side, we can pivot to the database from now on.
2. [I2]Tutor: "Please try to ensure that the work is more evenly balanced or that the times recorded are a bit more accurate." [check]
3. [I3]Tutor: "A review of the schema with a focus on cardinality and normalising the structure is recommended. Most likely, every table becomes a class/package in your backend code, these small tables will pollute your code." [the schema file has been updated and synced to the landing website]
4. [I4] [misunderstanding] As was described in the audit 2 presentation, the communication with the client is flexible. Usually, Wo communicates with the client about the requirements for both portal and database side, and the rest of the team engage in the process whenever they are needed (Wo calls them by phone or via wechat, and teammates respond fairly quickly if you are curious how it works behind the scene)

### Decision Making

**Good**

Tutor: "Your decision log provides a good breakdown of the rationale of each decision."

**Bad**

1. [I5]Tutor: "...you log combines technical, team, organisational, and project decisions in one table."
2. [I6]Shadow: Decision making logs lack types of decisions being made.

**How to improve**

1. [I5]Tutor: "You might want to consider adding a category to each decision to help delineate them, or split into separate tables based on the decision category. Some of your decisions don’t need to be captured in the log...You decisions should capture information that will be of use to your future selves or new project members." [will start adopting this practice this week]
2. [I6]Shadow: "The decision making log can be improved by adding the type of decision being made e.g. communication, technical etc." [will do]

### Team Work

**Good**

Client and tutor: The team seems to be well coordinated and working effectively.

**Bad**

1. [I7]Tutor: "...be aware of the time needed for each team member to complete tasks and review your progress against previous weeks to ensure a fair division of work."

**How to improve**

1. [I7] [The way each member contributes to the project is doing his/her part of the job which is functionality-oriented. Since every functionality varies and costs different hours of work, we will try to balance it during the next iteration]. :question:

### Communication

**Good**

1. Client: "Their high level of communication has been maintained since the last audit."
2. Tutor: "It is noticable since Audit 1 that the entire time is more active participating in tutorials."

**Bad**

1. [I8]Shadow: "Since the team uses WeChat as their main form of communication, there is no way of assessing how well the team communicates with each other."
2. [I9]Shadow: "The discussions in the meeting logs are still pretty vague. There are actions for each meeting but we still don’t know the exact discussions that went on. Were all the members always in agreement? Is there someone in the team who acts as a devil advocate just to encourage discussions on alternatives."

**How to improve**

1. [I8] [Our team uses WeChat for the maximum workflow efficiency, as it really serves well as an instant messaging tool. We really love to hear the way to measure how well a team's communicating.] :question:
2. [I9] [Maybe later on, we can elaborate more on the actions and rationales in the discussions, besides providing external links...] :question

### Reflection

**Good**

1. Client: "The team is also happy to listen to our feedback."
2. Tutor: "It is great to see input into the reflection log from all team members."

**Bad**

1. [I10]Client: "...it’s worth noting that some of the technical difficulties they are encountering on the functional side of the website are very similar to last semester."

**How to improve**

1. [I10] [Updates: improved by implementing a lot of functionalites this semester, including the term break...]
