---
layout: post
title:  "Book launch: high performing DevOps enterprises"
date:   2021-06-20
categories: devsops book 
---

Together with my colleague Tim Drijvers I contributed to a book on high performing DevOps enterprise, a book by DevOn.

<h2>Small steps towards building trust in automation</h2>

High-performing organizations are able to balance the quick delivery of new ideas with keeping things running in a stable way. DevOps not only enables developers to bring those new ideas to life quickly, but it also helps them take ownership of them once they are in production. While DevOps brings many benefits, it can take a while before these are realized. Taking small steps will help teams build trust in automated processes and achieve the DevOps maturity that is needed to enable high performance. Once that trust is there, developers can focus on solving business problems and achieving a successful outcome, which is much more important than just the output.

<h3>Speed, stability, and outcome</h3>

High performance brings speed and stability at an ever-increasing rate. A high-performing organization is one that is capable of executing new ideas fast, while also being able to continuously evaluate the results. For a scale-up like Sendcloud, this speed aspect is vital to be able to enter new markets and get to a product market fit at a rapid pace. But moving fast and keeping things running stable at the same time is hard, and doing this at scale is even harder. This is why we moved to DevOps practices.
Once a product is delivered, it is the same for software as it is with many other things within an organization: It is the result and usage which determines if an idea is successful. In other words, outcome is more important than output. To focus on outcome, you need to have flexible teams that can adapt to business plans which change because of this continual learning.

<h3>DevOps enables developers to realize new ideas</h3>
DevOps is all about enabling developers to deploy, run, and monitor their own applications. The role DevOps plays in building a high-performing IT organization is that it enables teams to bring new ideas to life quickly. With a focus on DevOps, development teams can bring changes to production faster, and it also helps them to take ownership once it is in production.

<h3>A DevOps implementation needs time to mature</h3>

For Sendcloud, DevOps is a way of working where a team provides a platform that other teams can use to build, deploy, and run their applications independently. In other words, these so-called feature teams can be responsible for both development and operations themselves, instead of having one team for development and another for operations. While this brings the benefits of quick idea realization and ownership, it also comes with some challenges.
One of the biggest challenges is that DevOps is only successful when it reaches a certain level of maturity. Taking Continuous Delivery (CD) as an example, in order to do this successfully you need to have good test coverage in your Continuous Integration (CI) pipelines, and a completely automated deployment process. Both of these are hard to get right straight away, especially when an organization is in the middle of transitioning from a more manual deployment process. You have to get to a certain level of maturity before the development teams will trust an automated system over a manual one.

<h3>Overcoming manual testing bottlenecks</h3>

Previously working at a SaaS company and at an online marketplace, we faced and solved the same issue of manual testing. In both cases one of the first steps we made was to break up the codebase into smaller pieces. We organized autonomous teams in a way that they worked on their own pieces of the codebase, independently of other teams. It also helped to have a self-service platform. The teams started to deliver faster in parallel, but the number of releases was still low. This was because the regression test was executed manually and as functionality continued to grow, it essentially became a bottleneck. Teams had to wait in line for the test to be run. Even with the number of test engineers we had, we could not keep up with the speed of delivery. So we decided to temporarily extend the test engineering capacity and removed the bottleneck. After that the teams could run a regression test for each feature on an isolated test environment that was launched via the self-service platform. As a result, they began to deploy with confidence, and even started deploying right before the weekend.

<h3>Gaining trust in CI pipelines</h3>

In the early days of continuous delivery at Sendcloud, broken code just got pushed to production, which eventually caused downtime of the platform. While the CI/CD setup was still in development, the gut instinct was to move back to manual deployments. This initial reaction was caused by a lack of trust in the CI pipeline. There had been other minor incidents slipping through the pipeline before, but nothing causing severe downtime. Every deployment is a risk, and it is hard to get CI/CD up to a level where you can just “click and forget”, safe in the knowledge that every deployment will have zero to minimal impact. Instead of just reverting back to the old manual setup, we decided to have a period of low or less risky deployments. Meanwhile we heavily invested in increasing the maturity of our CI.

<h3>Build trust and a strategy that covers all angles</h3>
To deal with these challenges, you need to build trust and take steps in several different directions at the same time to start to see the benefits. At Sendcloud we created a strategy to:
1. Move to smaller services that are loosely coupled;
2. Continuously integrate and deliver these services in parallel;
3. Get teams using a self-service platform that scales.
If you take just the step of implementing CI/CD practices, for example, without moving to smaller, loosely coupled services, you only get part of the benefits. The tech strategy at Sendcloud aims to do it all in parallel, but we still use Agile best practices to do it in small iterations.


<h3>Standardization and focusing on outcome</h3>

From a technical point of view, standardization is very important at Sendcloud. One example of this is that containerization and Kubernetes are becoming the standard. Large corporations are heavily investing in bringing these technologies to the masses and maturing them further. Another example is OpenTelemetry: standardizing events and how you send events to your metrics platform. This gives us flexibility to change our metrics platform, and it also limits vendor dependency.
When it comes to looking at the more organizational angle, it is important that people and teams can focus on outcome instead of on the details of the platform. This again helps you deliver ideas that are considered successful. Standardization of platforms also helps to focus on outcome instead of output.

<h3>A future where engineers can focus on solving business problems</h3>

Over the last few years, platform providers have been adding abstraction layers higher and higher in the stack. For example, it has changed from machine instances as a service to Functions as a Service. This is likely to continue and will allow engineers to focus more and more on actually solving business problems.
For Sendcloud specifically, this also means that we are providing more and more platform services that support DevOps practices. This helps teams focus on building solutions. We may even move to Function as a Service, Database as a Service and Queuing as a Service, as increasing levels of abstraction help us become high performing.
Regardless of what technologies the future holds, it is unlikely that teams will ever move back to a separation of development and operations teams – this is firmly in the past.

<h3>Dutch market has room to grow with respect to DevOps</h3>

There are many ways to look at how mature the Dutch market is in respect to DevOps. First, there is the labor market. From the perspective of attracting and developing talent, you need to apply DevOps practices as that is what people want. Engineers these days do not want to be dependent on others, they want to take ownership, they want to make their own decisions on how to do things. So Dutch companies need to move in this direction, otherwise they will lose out to competition when it comes to hiring.
The second angle to consider is consulting companies. They need to be willing to run what they build for you. Nobody needs partners who do the build and then leave the running up to you. If they do not take responsibility for how solutions run, it ultimately delivers a sub-optimal result for the customer.
Finally, if we consider software vendors, there are not many Dutch companies that are strong in platform features. Elasticsearch is a nice success story. However, other companies have a hard time as the large cloud vendors like AWS, GCP, and Azure keep moving up in the stack and offering more and more competitive services.
