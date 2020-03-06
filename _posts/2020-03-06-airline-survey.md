---
layout: post
title: Improving Customer Satisfaction in the Airline Industry
image: /img/airplane.jpg
subtitle: A key driver analysis of airplane passenger survey data.
---

If you went around asking what the airline industry could do to make their flights more enjoyable, you’d certainly get a few different answers. Better legroom, more comfortable seats, maybe food that doesn’t suck and a movie that isn’t terrible? They could try to make the perfect flight, but there’s only so much they can do. So the question is, what should a company focus their time and money on? 

To answer this question, I took a dataset that contained the survey answers from airline passengers. They were asked some information about themselves, including age, gender, and if they were flying on business or personal reasons. Then, they were asked to rate various services, on a scale of one to five, or zero if not applicable. Lastly, they were asked if they were overall satisfied or dissatisfied with their flight. 

![alt text](https://github.com/BuildABuddha/AirlineSurveyProject/raw/master/images/image_1.png "Confusion Matrix")

Using this data, the first thing I did was apply it to a random forest model. It didn’t take much work at all to get an accuracy of over 95%, which I thought was a high enough accuracy to spot some patterns in the data. Assuming my model is correct, it came to some pretty interesting conclusions, perhaps not what you’d expect. Here’s the most interesting and important findings. 

## What’s the deal with airline Wi-Fi?

By far the most important number on the survey was what rating they gave the Wi-Fi. This might come as a surprise, but it does make sense if you think about it. Access to the Wi-Fi is something you pay extra for, and it’s not fun to pay extra for something that turns out to be sub-par. Those that did not use the Wi-Fi and gave a zero were more likely to be happy than those who did pay for Wi-Fi and rated it one to three stars, with the happiest customers being the ones who used the Wi-Fi and rated it five stars. 

![alt text](https://github.com/BuildABuddha/AirlineSurveyProject/raw/master/images/image_2.png "Wi-Fi Service partial dependency plot")

What’s interesting to note is that while both business travelers and personal travelers hate having bad Wi-Fi, the personal travelers had the most negative reaction to it. This leads to my next observation, the difference between these two types of fliers. 

## Are you here for business or pleasure?

Those who were flying on business were, overall, much more satisfied than those who were not. This is perhaps because the majority of business fliers were seated in the more comfortable business class (roughly two-thirds of them in the survey). However, I suspect that a key factor is that their travel expenses are paid for by their employers. When it’s not your money paying for a service, it’s understandable that you’re less critical of it. 

![alt text](https://github.com/BuildABuddha/AirlineSurveyProject/raw/master/images/image_3.png "Online Boarding partial dependency plot")

As mentioned previously, these two types of customers have slightly different priorities. Another rating on the survey asked how satisfied they were of the pre-flight online boarding system. Those flying for personal reasons apparently had no strong feelings one way or the other for this service, but for business travelers, it was one of the most important factors to their overall satisfaction. 

Interestingly, I did the same analysis between male and female fliers and found absolutely no difference between them. Gender is, at least according to my model, completely irrelevant. 

## Comfort and convenience!

Besides Wi-Fi and pre-flight online boarding, here’s a list of the other services rated by the model, in order of most to least important:

* Check-in service
* Baggage handling
* Seat comfort
* Inflight service
* Cleanliness
* Inflight entertainment
* Leg room
* Gate location
* Ease of Online booking
* Departure/Arrival time convenience 
* Food and drink

![alt text](https://github.com/BuildABuddha/AirlineSurveyProject/raw/master/images/image_4.png "Shaply Plots for satisfied and unsatisfied customers")

Above are visuals showing the impact the model predicted on four different people interviewed in the survey. The first two were satisfied, the last two, not so much.

Of note is that the last four items in the above list were next to inconsequential in importance, at least according to the model. Wi-Fi and pre-flight online boarding were usually the deciding factors, but the top five features in the above list also helped the model decide if a customer would ultimately be satisfied or dissatisfied. 

[Click here to check my work!](https://github.com/BuildABuddha/AirlineSurveyProject "Hazardous NEOs GitHub Repo")
