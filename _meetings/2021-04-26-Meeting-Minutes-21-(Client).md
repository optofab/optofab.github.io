---
layout: post
---

> Date: 23th April 2021<br>
> Time: 11:15-12:20pm<br>
> Attendance: Wo Tian, Hengrui Xu, Guoyu Wang, Clients

{% include toc %}

## Details

### Order:

    -Parts 1m
        -Design 11
        -Materials/COGS (cost of goods sold) 11
        -deposition/production 11
        -postproduction 11
    -Finance/Legal 11
    -Customers 1m
    -Action required (bool) 11
    -Action Notes 1m

(want to choose to add dropdown options)

### Customer (multiple per order):

- Name 11
- Title 11
- Phone (+country code) 11
- Email 11
- Ship Address - 1 per order
- Bill Address - 1 per order
- Organisation (1 order to 1 org)
- Role - shipping, finance, etc 11
- Type – Industry, Academia, Overseas 11
- Sector – laser, defence, etc 11

### Finance/Legal:

- MTA (link, ideally open straight away, at least file location) 1m
- Quote (id) [id, link, date, description] 1m
- Job cost (calculated number) 11
- Invoice (link) 11
- Current quote date (date) 11
- Invoice Date (date) 11
- Payment reminder (date) 11
- Payment reminder sent (bool) 11
- Payment received (bool) 11
- Action Required (bool) (Opto action required) [id, type of actions, section] 11
- Action Notes 1m
- Payment Due Date (Date) (if exceeded auto-action) 11

### COGS/Materials:

- Object-Name (char) 11
- Cost (money) 11
- Quality (int) 11
- Supplier (org, text) [id, org, contact name, phone, receipt] 11
- Date Purchased 11
- Date shipped 11
- Date received 11
- Quote (link) 11
- Description (text) 11
