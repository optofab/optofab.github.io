---
layout: landing
permalink: /project-requirements/
tag:
  - "Database"
  - "Website"
---

> Our project comprises two inseparable parts: **database** and **website**. For the database branch, it is essential to implement the following functions:
>
> - Integrate the data related to the ordering procedures into the database for management and analysis
> - Store client order specifications, links to metrology, and operational information
> - Store links of supporting documents for future modifications

{% include toc %}

## Database Requirements

### Basic Requirements

- [Requirement] Ensure the security against data breach and information theft.
  - [User Story] The database contains sensitive info about the customers who take privacy seriously.
  - [Importance] :red_circle:
  - [Notes] Offline database for highest level of security

<hr class="hr-dotted">

- [Requirement] ANFF staffs can import order data from online request
  - [User Story] Deon wants to import order data from online request automatically, so that he can minimise the risk of human errors.
  - [Importance] :red_circle:
  - [Notes] Automatically parse the website information and load them into the database

<hr class="hr-dotted">

- [Requirement] ANFF staffs can search for data entries
  - [User Story] Steve wants to search for data entries by an attribute, so that he can retrive information efficiently.
  - [Importance] :red_circle:

<hr class="hr-dotted">

- [Requirement] ANFF staffs can sort the data entries
  - [User Story] Steve wants to sort the data entries by an attribute, so that he can compare the similar data.
  - [Importance] :red_circle:

<hr class="hr-dotted">

- [Requirement] ANFF staffs can use the database offline
  - [User Story] ANFF staffs want to use the database without internet connection, so that the data security can be guaranteed.
  - [Importance] :red_circle:

<hr class="hr-dotted">

- [Requirement] ANFF staffs can see the inofrmation about an order
  - [User Story] Steve wants to see the information about an order, so that he can understand what the customers need.
  - [Importance] :red_circle:
  
### Technical Requirements 

| Languange/Tool | Application Field                                                                            | Extra Packages/Libraries |
| -------------- | -------------------------------------------------------------------------------------------- | ------------------------ |
| .Net/C#         |- Full stack development                                          |TBD|
MySQL | - Database |

<br />

## Website Requirements

> The website will be used for customers to submit their order and track order status, in addition, the website should send the submitted order to the manager through e-mail.

## Assumptions

- Customers will submit and track their order on the website

- The website should not show any confidential information, including the design of the product or the customer information

### Basic Requirements (User Stories)

- [Requirement] Customers can submit their order requirements

  - [User Story] Customers can place order in the website and submit their relevant document like pdf to explain their requirements.
  - [Importance] :red_circle:

<hr class="hr-dotted">

- [Requirement] Submitted order will email to the manager

  - [User Story] Steve wants all submitted orders send to the manager via email, so that they don’t need to store any information on the backend of the website.
  - [Importance] :red_circle:

<hr class="hr-dotted">

- [Requirement] Customers can check status of their orders
  - [User Story] If customers need to track their order, they can check the status of their order updated by ANFF staffs manually.
  - [Importance] :warning:
  <hr class="hr-dotted">
  
- [Requirement] Customers can submit feedback through the website
  - [User Story] After the order completed, the customer may want to provide their feedback, so that the Physics team can collect them from customers.
  - [Importance] :warning:
  <hr class="hr-dotted">

- [Requirement] When customer submit their full order, a confirmation e-mail will be sent to their e-mail address
  - [User Story] Customers want to receive a confirmation for their ordering, so that they know they have placed the request successfully.
  - [Importance] :red_circle:

### Technical Requirements

| Languange/Tool | Application Field                                                                            | Extra Packages/Libraries |
| -------------- | -------------------------------------------------------------------------------------------- | ------------------------ |
| React.js         |- Front-end design and functionality                                               |react-router-dom, formik|
| CSS 3/4        | - Webpage styling                                                                            | Bootstrap library        |
| PHP 7.3.24     | - Back-end functionalities                                                                   | PHPMailer library        |
