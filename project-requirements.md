---
layout: landing
permalink: /project-requirements/
tag:
  - "Database"
  - "Website"
---

> Our project comprises two inseparable parts: **database** and **website**. For the database branch, it is essential to implement the following functions:
>
> - Protect customer privacy from leaking out
> - Integrate the whole data related to the ordering procedures into the database for management and analysis
>   Store client order specifications, metrology, and operational information
>   Track costs and usages of materials and services
>   Support documentation for future modifications

{% include toc %}

## Database Requirements

### Basic Requirements (User Stories)

- [Requirement] Must be secure against data breach and information theft.
  - [User Story] The database contains sensitive info about the customers who take privacy seriously.
  - [Importance] :red_circle:
  - [Notes] Offline database for highest level of security

<hr>

- [Requirement] Need a convenient way (identifier) to match customer company to the ones already in the database without confusions
  - [User Story] John is a customer from Reflection Optics Inc. who orders a standard coating. On the webpage, when asked to type his company name, he might enter Reflection Optics Inc or Reflection Optics or ROI for short. The database needs to record this correctly in order to avoid mismatches and confusions.
  - [Importance] :warning:
  - [Notes] Using email domains; ABN or link to other validation system

<hr>

- [Requirement] Must be able to minimize human errors when updating the databases
  - [User Story] Deon wants to update the database with a new design. During the process, if Deon was asked to type the file name or other info by hand, there is always a possibility of misspelling because everyone makes mistakes. So the interactions and operations of the database software must minimize manual typing and checking.
  - [Importance] :red_circle:
  - [Notes] Automatically generate metadata of files and load info into database

<hr>

- [Requirement] Must be flexible enough for staff to supplement new info later or add new designs or modifications
  - [User Story] Johannes wants to experiment on new material for the customer, but not sure of the specifications right now. He can create a record in the database, and update and add more info later on to complete the design.
  - [Importance] :red_circle:
  - [Notes] Links to new design files; Tags/hashtags added manually when updating; Versions no. for different designs

<hr>

- [Requirement] Must be searchable for easy lookup
  - [User Story] Steve wants to check the percentage of a certain wavelength of all orders to optimize coating procedures. By searching for a wavelength keyword or type in a certain range, the database should show him the corresponded records.
  - [Importance] :red_circle:
  - [Notes] Using tags to manage records

<hr>

- [Requirement] Need to figure out a way to sync between different nodes of computers across several labs, while preventing conflicts when multiple staff try to update record at the same period of time
  - [User Story] Both Deon and Johannes are in charge of a new design, so they need to test the coatings in different labs and write in the database their own parameters. When Deon is updating the file, Johannes should not be able to change the same field to avoid conflicts.
  - [Importance] :warning:
  - [Notes] Perhaps utilising the Physics network; Using USB on local computer to copy data

<hr>

- [Requirement] Must be able to prompt a warning banner to staff when his operations are incomplete or false
  - [User Story] Deon just finishes updating the specifications of a new design but forgets to add the version number. The software needs to remind him of the lack of version field to complete the accurate update.
  - [Importance] :red_circle:
  - [Notes] Set up required fields that match primary keys in the database

<hr>

- [Requirement] Key data in the database should only be accessed by staff in charge
  - [User Story] Steve recruits a new intern to help him with the design, but the intern should not be able to change the key fields of the database right away until Steve thinks it is time and grants him a higher level account
  - [Importance] :warning:
  - [Notes] Different levels of authorizations to access database

<hr>

- [Requirement] The data in the database needs to have regular back-up copies
  - [User Story] Since many data will be stored in the local computer.What if the computer system crashes? Then all the data will be lost even if there is no data breach.
  - [Importance] :red_circle:
  - [Notes] Have a local back-up copy

<hr>

- [Requirement] The interface needs to be user friendly
  - [User Story] The development of the database must be based on the the users requirements and our clients wish it can be easy to use.
  - [Importance] :red_circle:
  - [Notes] Set up drafts of the interface during the design part and can be modified

<hr>

- [Requirement] It will be better if the back-end doesn’t need the programmer maintence.
  - [User Story] Steve wishes we can build the database that can be long term use without the techinical maintenance
  - [Importance] :large_blue_circle:
  - [Notes] Do not put so many contributes in the main table to avoid the redundancy; The data base has to be flexible for future needs.

<hr>

- [Requirement] Need to have a way to update the website database (once a day) to update client tracking data.
  - [User Story] The staff Jack needs to be able to either schedule an automatic update or manually update the order status so that clients can track their orders from time to time.
  - [Importance] :red_circle:
  - [Notes]

<hr>

- [Requirement] Must be easy to update the website database automatically when there’s new record in the main local database
  - [User Story] When Deon types in a new order specifications and updates the main database, the website file should be able to update accordingly for the customers to track order status. For now, a daily sync is enough.
  - [Importance] :warning:
  - [Notes]

<hr>

- [Requirement] Need to notify the administrator for the new update in the main database
  - [User Story] Johannes/Steve/Deon needs supervise the design sometimes to ensure that the database is well maintained.
  - [Importance] :large_blue_circle:
  - [Notes] A push notification may suffice

### Technical Requirements (TBD)

## Website Requirements

> The website will be used for customers to submit their order and track order status, in addition, the website should send the submitted order to the manager, and the matched database should provide the information about the order status in order to provide a tracking function.

## Assumptions

- Customers will submit and track their order on the website

- The website shows no secure information, including the design of the product or the customer information

- All queries on the website should be documented

### Basic Requirements (User Stories)

- [Requirement] Customers can submit their order requirements

  - [User Story] Customers can place order in the website and submit their relevant document like pdf to explain their requirements.
  - [Importance] :red_circle:

  <hr>

- [Requirement] Submitted order will email to the manager

  - [User Story] Steve wants all submitted orders send to the manager via email, so that they don’t need to check the website.
  - [Importance] :red_circle:

  <hr>

- [Requirement] Customers can check status and status only on the website
  - [User Story] If customers need to track their order, they can check the status of their order, but no more detail will show in the website.
  - [Importance] :warning:
  <hr>
- [Requirement] A database to store tracking detail
  - [User Story] Order status will be stored in this database, database will be uploaded manually or regular update from another database. When customer send tracking request, the website will load data from this database.
  - [Importance] :red_circle:
  <hr>
- [Requirement] The website need to receive customer feedback
  - [User Story] After the order completed, the customer may want to give their evaluation or suggestion, and the Physics team also want to collect ideas from customers to enhance their product.
  - [Importance] :warning:
  <hr>
- [Requirement] The website need to send a email to customer to active email address
  - [User Story] Steve wants to send full order information to customer via email, so it is essential to confirm customer provided the correct email address, or their information will be leaked.
  - [Importance] :warning:
  <hr>
- [Requirement] When customer submit their full order, a email with all information will send to their email
  - [User Story] Customers can only track the order status on the website, so they need to receive an email include their full order information.
  - [Importance] :red_circle:

### Technical Requirements

| Languange/Tool | Application Field                                                                            | Extra Packages/Libraries |
| -------------- | -------------------------------------------------------------------------------------------- | ------------------------ |
| HTML 5         | - Website structure<br>- Front-end design                                                    |                          |
| CSS 3/4        | - Webpage styling                                                                            | Bootstrap library        |
| JavaScript ES6 | - Website functions<br>- User interface interactions<br>- Front-end & back-end communication |                          |
| PHP 7.3.24     | - Back-end functionalities                                                                   | PHPMailer library        |
