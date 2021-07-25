---
layout: post
---

> Date: 23th March 2021<br>
> Time: 14:00pm - 16:15pm<br>
> Attendance: Wo Tian, Wu Tian, Hengrui Xu, Ruiqiao Jiang, Guoyu Wang, Yaoyi Xu, Ruoqian Wu, Client

{% include toc %}

## Agenda

1. Discuss the website prototype

## Discussions

1. Need to modify the website prototype to better meet the user requirements.

## Action

1. Modify the website prototype.

## Next meeting

Date and Time: 18:00 25/03/2021

## Detailed discussions

For the new order part, when requesting the form, we need to add “no selected” in the drop-down box.
First, if the geometry is oval, replace ph1 and ph2 with major and minor parameters. We need to add the unit (diameter, mm) after each box (thickness, height, and weight). For the curve part , we need a number representing the curvature, for example, 0 represents flat,1 represents toric,2 represents parabolic and some on. And if the customer chooses parabolic, it will pop-up a message “please give us more information”. We can choose to use numbers instead of the drop-down box for the selection, because there may be many different curves. We need to put more pictures and diagrams on the website to make customers fully understand.

For the customer, maybe they have two various coatings, they can modify their request. For example, after they finish their second coating part on the website, they can still go back and modify their first coating design. And their second design part will show underneath their first design. We can have three buttons like submit(means customers have finished their design), add another coating, previous page/back. If there are more than two coatings, the customer needs to fully describe. When the customer wants to add another coating, they will repeat the same process of filling out the form. We need to think about how we can store the temporary data, so when the customers go back to the previous page, there will be no data missing. And we can also add a cart, which can be “checkout” without signing in and registering.
Second, if the geometry is rectangular, the same as the oval, we need to add units after the weight, height, and thickness.
And we need to add one tap box called the number of sides below all this information. (how many sides will be coated/or they don’t need coating)If the clients only want to do one side coating, it appears as coating side 1.
When uploading the file, we should limit the size of the file(2MB for example). And only the pdf version and png version can be accepted. The customers can upload the files by drag and drop or select the file.
For the tracking part, we need to add more details.
When the clients submit this form, they will receive the email with all the information automatically.(in different format/with an attachment)
Below the addition specification, there will be several text box: shown in the picture.

<img src="/images/whiteboard-prototype-1.png" alt="white-board-prototype">

Surface finishes-surface roughness/form accuracy/surface quality（three parameters)
Toxicity: choose between inert and reactive.
Material: toxic and other dangerous exposure chemical material

<img src="/images/sketch1.png" alt="sketch-1">
 <br>
<img src="/images/sketch2.png" alt="sketch-2">
