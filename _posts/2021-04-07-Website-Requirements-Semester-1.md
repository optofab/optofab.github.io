---
layout: post
tag:
  - "Project Requirements"
  - "Website"
---

> The website will be used for customers to submit their order and track order status, in addition, the website should send the submitted order to the manager, and the matched database should provide the information about the order status in order to provide a tracking function.

## Assumptions

- Customers will submit and track their order on the website

- The website shows no secure information, including the design of the product or the customer information

- All queries on the website should be documented

## Details

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
