---
layout: post
title:  "Low code through the eyes of a traditional programmer"
date:   2020-05-19
categories: low code linkedin
---

<h3>30 second summary</h3>
Low code helps deliver fast in these scenarios: 
- Simple transactional applications 
- Solutions for internal use 
- Test a new business concept or product 
- Small development team 

With more complexity you get limitations for multiple reasons: 
- Low code platforms are not designed for large-scale parallel development and deployment 
- It works best when you relax the business requirements (keep it simple) 
- In contrast to its promise: people with the right skills are hard to find 
- It is not-so-low-code after all, but more of a productivity platform 
- You do not have full control of performance 
- They scale sub-linear (vertical scaling and shared resources) 
- High availability issues because of large fault domains due to tightly coupled design 

With proven patterns you can leverage the benefits of low code in the 4 scenarios and avoid the limitations when complexity increases. 

<h2>Introduction</h2>
During the last 12 months I have worked on two products using a low code platform. One was a back-office application and the other an online marketplace. For one of these the team used BettyBlocks and for the other one we used Outsystems. 

Initially I was sceptical about low code platforms. Now I am positive if you use it for the purpose it’s designed for. And that is where things in IT often go wrong: people use technology in places where it might not be the best fit, because it is all they know or maybe because it is a hype. Expectations are high, but soon disillusion kicks in. In this post I would like to share with you how I would get most value using low code platforms and how to avoid disillusion. In terms of the Gartner hype cycle I hope to bring you to the plateau of productivity with low code platforms. 

First, I keep in mind the 2 main goals of any software technology organisation according to the book Accelerate (Forsgren, Humble, Kim): 

1. Deliver solutions fast 
2. Run stable in production 

The reason I take this approach is that any solution I choose to solve a problem, needs to help me deliver faster and run more stable. If it does not help a team to be fast and run stable, then you might need another technology for your specific problem. Also, it might be that a low code solution works well for you today, but not in the days after. For example, because your solution works when it is small, but not at larger scale. I’ll get to this later. 

Second, I distinguish between 2 solution areas: 

1. Simple transactional applications, or CRUD-applications (Create, Read, Update, Delete) with basic forms that users use 
2. More complex web scale applications  

For the first think about internal applications to simply maintain records. For the second think of web shops, marketplaces, complex user flows, cross device solutions, etc. 

Think about it on a scale of good fit to not-so-good fit:

![scale_simple_to_complex](https://user-images.githubusercontent.com/5676977/143087445-8d8a020c-a370-4779-a492-65bcad88376f.png)

If you have a simple scenario, then I would say go for low code (if you can afford the license costs). If your problem looks more like the complex scenario, then continue reading. 

<h2>Low code and speed: it’s for a sprint, not a marathon</h2>

In the graph below I visualised how in my experience speed evolves over time in a low code environment compared to a hand code solution. Of course, I assume that the hand coded solution is done well: modular, horizontally scalable, etc. 

![speed_and_scale](https://user-images.githubusercontent.com/5676977/143087444-e91b5a3a-ad87-46ce-8639-cf620558352a.png)

What I want to illustrate is that low code is fast at first. There are a few reasons for that: 
- There is hardly any boiler plating involved, so you can start right away and deliver value from day 1 
- There are many off-the-shelf components available that you can use quickly 

Once you grow however, you get diminishing returns: you may double your team in size, but you don’t get twice the output. The two main reasons for that are: 

1. low code platforms have been designed to deliver functionality fast, but they hardly focus on non-functionals (maintainability, scalability, availability and many other ‘-ilities’) 
2. low code platforms are still a bit behind on modern development practices for larger teams, for example it is hard to do dark launches or canary releases, zero downtime deployment is often not an option, backing services like the database are shared. 

So this is, in my opinion, the design trade-off of low code: you get functionality fast, but it comes at the cost of non-functionals. Once you get bigger that’s when it’s going to hurt, so you need to plan to avoid that. 

![nfr](https://user-images.githubusercontent.com/5676977/143087442-87e795c6-c61d-41de-9332-991e81a23d36.png)

I am not stating that all low code platforms are bad in non-functionals. It is just not their strength, but a result of the trade-off they made. You need to consider that to avoid disillusion. Below I share a few of these considerations. 

<h3>Not designed for parallel development and deployment</h3>
Low code platforms tend to have monolithic codes bases. That is not necessarily a bad thing: monolithic design is a pattern just as service architecture or modular architecture is. In certain scenarios it works well, but it comes with some challenges though: if you deploy to production you deploy everything. As a result, all work needs to be completed, there cannot be any work in progress.  

A workaround could be to implement a feature toggle solution yourself, so that functionality is turned off by default and can be turned on when ready. Then you can deploy the monolith while it still has unfinished work. This does not come out-of-the-box mostly, so you must build this yourself. 

Note that when you plan to continue with a small team, this is not an issue. When you plan to scale up however, you need to act accordingly when using a low code platform to avoid the slow down as illustrated. 

<h3>Relax the business requirements or it won’t be so fast after all</h3>
Basic solutions can be developed fast without too much technical knowledge. However, with more complex requirements you quickly reach the limits of the capabilities of the platform. Some platforms cannot support them, while others allow for more custom development. With custom development you do not get all the low code benefits in terms of speed and required knowledge. If you make it too complex, do not blame the low code system when you run into issues: they are not designed for that. Keep it simple or choose another solution, that better fits your needs. 

<h3>Attracting talent is hard and might slow you down</h3>
In case you are successful with your business you maybe want to scale up in team size. Also, in case you decided to do more custom development instead of keeping it simple, you need more developers to implement the functionality.  

This is also where disillusion often starts: it is very hard to find the right people at a decent price. For hand coding you need capable engineers, and due to the availability of many open frameworks, there is relatively high availability. Low code platforms are proprietary systems with a much smaller community of developers. It is very hard to attract talented developers and consulting companies are willing to help you, but not for the lowest costs. The benefit of speed can easily be undone by the lead time to attract people and the costs that come with that. 

<h3>A productivity platform instead of a low code platform</h3>
Above I stated that you need to lower requirements and keep it simple, so you keep having the benefit of speed. Reality however is that this is very hard. In that case low code becomes not-so-low-code and you get closer to hand coding. In this scenario I see these platforms more as solutions to boost productivity of developers. Developer productivity platforms instead of low code platforms. However, at larger scale (multiple teams, larger code base) you still become less productive for the reasons mentioned above. 

The examples above impact speed. Some non-functionals also impact stability in production. These are outlined in the next section. 

<h2>Low code and stability: it works today, but will it run tomorrow?</h2> 
When you deliver fast, your customers or stakeholders will be happy, unless you have low performance or frequent downtime. If you cannot use the system, then it is still not of value. That is why in this section I share my experience on stability of low code platforms. 

<h3>No full control on performance</h3>
As stated in the definition above, low code helps you building software with graphical configuration instead of hand coding. This results in (1) generated code and/or (2) meta-data that needs to be retrieved run-time. Both result in relatively slow performance. I state ‘relative’, because for internal applications 3 seconds to load a page might be acceptable, but for e-commerce purpose it is not. Now you can analyse a page request using load test tools and real-user monitoring solutions to find the bottlenecks, but you can only tune it to the extent that the low code platform allows you to do. Combined with the points below this might give issues at larger scale. 

<h3>Vertical scaling is limited</h3>
Low code platforms often have a back-end and a front-end layer. For some the front-end is split up in an API layer and a UI layer. 

The back-end layer is mostly a relational database. These databases are designed for consistency and availability and not so much for scalability. So relational databases are a very good choice when you need consistency and availability, but if you need scalability you need to be aware that you are bounded here: you can only scale vertically by getting a bigger server and that will increase the costs of your license fee. Some relational databases support horizontal scaling, but most low code platform do not support these databases. 

The database choice in low code is not just resulting in scaling challenges. See the next paragraph for that. 

<h3>Tightly coupled design results in single points of failure and large fault domains</h3>
Most platforms have a shared database server. That means that when you have multiple applications or multiple modules within applications, they all store their data in the same database. Besides that, these applications often share the same application server, resulting in application issues often impacting other applications as well. For example, if one application has a run-away query, all other experience lower performance. Or if one application needs down-time for deployment, all other applications experience down-time. 

Most platforms offer a High Availability setup and you can use that to limit these drawbacks. However, that again comes with a price that is relatively high compared to other types of solutions. 

So far, I listed some things to consider when you plan to use low code platforms on a larger scale and for more complex applications. For both speed and stability, I listed three considerations. Based on these you probably already get to the cases where low code platforms work well and where they do not work so well. Let me now give you some example cases as well as recommended patterns. 

<h2>Cases where low code works fine: when large scale and stability are not (yet) important</h2>
You might feel that low code is not for you after reading all the above. But like with many IT solutions, it might be a good fit. As said, when you use it as intended, when you leverage its strengths and when you plan for solving weaknesses. In my opinion the following cases are a good fit for using a low code platform: 

![cases](https://user-images.githubusercontent.com/5676977/143087440-e0857a10-fcbf-4cc1-8274-76473c8db12c.png)

You can grow your way out of these characteristics in several ways: 
- Your simple application evolves into a more complex one 
- An internal application is exposed to the outside world with different needs/service level 
- Your new product resonates well and your user base increases 
- Due to higher demand your team grows 

These developments are positive and without your low code platform it might have taken longer to get to this. Now you need to take care of not getting limited, because you enter territory where low code is a less good fit. Therefore, I recommend planning for the following patterns or growth path. 

<h2>Recommended growth path</h2>
While your stakeholders or customers are still happy you need to start the discussion on what it takes to keep them happy. This is not always easy because (as illustrated below) this is all about architecture and paying off technical debt. Both are invisible items compared to features and bugs. 

![tech_debt_quadrant](https://user-images.githubusercontent.com/5676977/143087438-d58d4391-54b4-4786-afcb-8669fccd5fcc.png)

People have plenty of time to discuss features and bugs, because they are visible, valuable and tangible. In contrast, architecture and technical debt are more abstract and have no immediate value. That is why you need to plan for it as of day 1. When you start your first day building a low code application, also initiate the discussion that is needed to set expectations and keep everyone happy. For doing this I recommend multiple phases that balance short term goals with long-term needs. 

![transition_path](https://user-images.githubusercontent.com/5676977/143087436-66ac20f8-9b8e-46fa-be0a-428f5359881a.png)

<h3>1 - Learning phase</h3>
You start off with your simple application. There is no outlook for more complex requirements, so you do not want to do premature optimization.  

Or maybe your new product or business concept has not even been tested. You have expectations, you have a design and a target group to test with, and now you need to ship as soon as possible. Also here just use your low code platform with all its features to go fast. 

In both cases there is no need to handle high usage volumes or support large development teams. However, do start setting the expectations for the following 3 steps.  

<h3>2 - Decouple back-end and front-end</h3>
I would start working on this step as soon as you get signs that your application is going to be successful. If not, then just leave it as is. Most platforms have the option to build an API layer on top of its database. Some might even do so by design. In the latter case you are all set. If not, then make sure your UI connects to an API layer that exposes the database. Preferably you build this within the low code platform to leverage its features for high speed. Later, in phase 4, you’ll move this to another platform. 

Solutions like this are often referred to as Back-end For Front-End (BFF) or a Gateway. 

<h3>3 - Scaling up the back end</h3>
Now that you have de-coupled front-end and back-end you can enjoy some benefits already: 

You can develop back-end and front-end independently at their own speed 
You can change the back-end implementation without (too much) impact on the front-end and the end users 
Let’s for example take a web shop. When you search for a product and you click on one, it opens a Product Detail Page. That page contains Product Content and Product Offer (delivery time, price, etc). Content does not change much. Offers change more often. Let’s say you have performance challenges with displaying Content and Offers and your analysis tells you the database performance is the bottleneck.  

In this case take out the Product Content and Offer functionality and put is in a separate service (not on your low code platform). You can build it yourself or choose a headless commerce platform like Commercetools. For that service you can choose the technology that fits for purpose, e.g. not a relational database, but a document store for Product Content where you retrieve all product information for a product ID with just one API call. 

Now reconnect the API layer to your new Product Content and Product Offer services and there you go: you now have a highly scalable part of your application without front-end or end user impact. This approach is referred to as the Strangler Pattern. 

You should put these improvements on your product roadmap and continually discuss them with your stakeholders. Over time you’ll end up with a highly scalable and high available set of back-end services that can be built and deployed independently from each other and from the front-end. 

<h3>4 - Scaling up the front end </h3>
If you just stop here, you already made some good steps. Your dependency on the low code platform is limited. You leverage its benefits for speed, and you introduced alternatives for speed-at-scale and stability. 

There might still be reasons why you want to introduce a new front-end: 
- More influence on performance 
- Leverage the latest front-end technology 
- Get less dependent on scarce skills of some low code platforms 
- Limit vendor dependencies even further 

What worked for the back-end works for the front-end as well. Thanks to the API layer in between you can introduce a new front-end on the same back-end. The current front-end on your low code platform can co-exist with the new one. As soon as the new one is on par you can sunset the old front-end.  

In addition, you can build different front-ends if you like one for each use case, device or channel.  

In the scenario where both the back-end and front-end have been moved away from the low code platform, you may also move the API layer somewhere, for example to a cloud platform provider. At this stage you have successfully used low code to launch your application, product or business and you moved to something that works at scale gradually. You can keep your low code license and platform for new initiatives. 

<h2>Conclusion: low code is a good choice when used as intended</h2>
Low code platforms are a nice addition to the available options for building a digital business. You do need to use it as intended. And it has its trade-offs. But that applies to all technologies. To avoid disillusion use it for the cases mentioned in the article (simple, small case, a new product to be tested) and plan well ahead in case your situation changes (more complex, large scale, proven product). If you do so, you get the benefits and avoid the pitfalls. As illustrated below you’ll be fast in the beginning and you’ll stay fast at scale. Where does the beginning phase end and where does larger scale start? That depends on the specific low code platform you choose.

![speed_and_scale_end](https://user-images.githubusercontent.com/5676977/143087432-28a68748-6b8f-4a19-87f8-ae15612889fc.png)

