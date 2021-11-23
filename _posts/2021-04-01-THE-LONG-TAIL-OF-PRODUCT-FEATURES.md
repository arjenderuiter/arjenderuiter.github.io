---
layout: post
title:  "The long tail of product features"
date:   2021-04-01
categories: product management long tail leaddev
---
_This article was initialy published on [The Lead Dev](https://leaddev.com/technical-decision-making/long-tail-product-features)_

<h1>The long tail of product features</h1>

_Growing from a product to a platform company with a small development team_

Product development has diminishing returns. You often have a first product serving all clients, and then you add functionality that is relevant to sub-segments only. Hence, the relative value for effort decreases. You can solve this by focusing on the core product yourself, and work with partners to provide additional solutions. This way you need limited development capacity yourself. This article explains how you move from a product company to a platform company; how you move from UI-first development to API-first development; how you keep a small development team and leverage partners.

<h2>Avoid diminishing returns of product features</h2>
If you work in a software-driven business, you probably recognize what I have learned throughout my years of working in Software-as-a-Service (SaaS) and e-commerce:

_You have limited development capacity. Therefore, you cannot build all the solutions you want. So, you have to make choices_

In other words, your software development team always feels too small. And because of that limited capacity, you prioritize goals or problems to be solved: you only build solutions that serve most of your customers.

You determine for which customers you can make the biggest impact, and what deliverables you need to build to do that. You focus on a customer group that sees big value in the solution – the solution being worth much more to them than the investment you made with your product development team.

You prioritize based on value for effort: you know how much the problem is worth solving to those customers; you know the effort needed to build the feature; you rank based on value for effort and thus optimize the allocation of your scarce capacity.

At a certain stage, you find that you have a large market share within the primary customer segments you focus on; you serve their needs well and you make a big impact. However, you want to grow further. For this you need to solve more problems, so you target sub-segments in your existing customer base or you need to appeal to other customer segments. In both cases, you end up in smaller segments that might be worth less, but the relative effort to build solutions for them increases.

A response often seen is to multiply development capacity to serve all these new segments. However, because these segments are less valuable, your value-for-effort goes down. Each next increase in revenue will require relatively more investment. Revenue will be sub-linear to investment and this is a bad situation to be in.

![diminishing_returns](https://user-images.githubusercontent.com/5676977/143083059-e52756ff-c281-4ce5-a4bb-babceacea720.png)
_Diminishing returns of product feature development – the value for effort decreases with each next best feature._

The long tail of product features
When I saw this pattern a few times, it reminded me of Chris Anderson. In his book, The Long Tail, he describes the following phenomenon in retail business:
- Few products get sold a lot: the head
- Most products get sold only a few times: the long tail

In his book, Chris outlines how brick-and-mortar shops have limited shelf space and need to focus on the profitable head. However, online shops can differentiate by offering the long tail because there is no constraint in terms of shelf space. The customers who want a product that is not sold often are willing to pay more for the product.

You can apply this pattern to product features, so you get the product long tail:
- Few features are used by all customers: the head
- Most features are used by a few customers only: the long tail

![long_tail](https://user-images.githubusercontent.com/5676977/143083056-b0bc9183-61e2-470a-8183-5f1695b11067.png)
_The long tail of product features  – a few features are used by most customers; most features are used by few customers._

By ‘customers’ I do not mean the primary segments you focused on first, I mean the customers you’ll target in the future with features you have yet to build. Currently, you focus on the head of features and the customer segments served with that, but now you want to grow further. You enter the domain of the long tail of features for sub-segments and new segments. The head was highly profitable, with high value for investment (the development capacity allocated to it).

But how do you make the long tail of product features as profitable? How do you make sure you do not require 100% increase in capacity for only 50% increase in value? This is where you can apply platform thinking to product development.

<h2>Think ‘platform first’ in product development</h2>
Let’s look at the ‘attract’ phase from the Marketplace model discussed in Platform Strategy by Laure Claire Reillier and Benoit Reillier.

In this model, you first attract both sides of the marketplace: demand and supply. In this case, you have customers with a need for solutions on one side and partners who can offer a solution on the other side. You can only do this in the following order:
- You develop a strong head that attracts sufficient customers from your primary segments
- You develop the tail with partners who target sub-segments and new segments

You can only do step two after a successful step one. In step two, however, instead of developing solutions with your own team, you develop a partner landscape: you choose one or more partners to fulfill each need. 

This way, what at many companies is called partner management, also becomes product management: your partners extend your own development capacity. For this to work, in step one, you need to build your core using the ‘API first’ principles. Or in other words, make every solution externalizable.

Navigating the long tail to your advantage
You developed a strong foundation and then you started to lever your customer base (one side of the network or marketplace) to attract partners (the other side). This way you multiply your speed of product development, without multiplying your development team. Now let’s take this further and see how you can move the long tail to your strategic advantage. There are three directions:
- Move up and increase overall adoption of features
- Move left and make partners responsible for the head
- Move right and take over solutions from partners

Moving up is what everyone wants to do. In SaaS this is increasing adoption, so that churn goes down. Most companies are used to doing this for their own product, but in this case, you need to work with partners to ensure features in the long tail are used a lot.

![long_tail_move_up](https://user-images.githubusercontent.com/5676977/143083053-2bf21b7d-bcde-41cf-80d1-91118b08182c.png)
_Move up the long tail by increasing the adoption of features together with your partners._

Moving left or right is a strategic choice, and you do one or the other per solution domain.

If you move left, you bring back your core product to a network or platform provider. Initially, you needed the head to attract one side of the network, but now that the other side is on board, you can bring back your core product to only provide the networking features. The core asset of the product is not the software anymore, but the core assets are now the network or marketplace participants (customers and partners). This is the ultimate position to be in. You have huge leverage on your product head.

![long_tail_move_left](https://user-images.githubusercontent.com/5676977/143083047-955ad769-f3ee-427d-a6ae-43084fca3a02.png)
_Moving left or right on the tail is a strategic decision._

Moving right is another choice. You can do so in two ways: acquire a partner, or develop your own substitute of a feature that a partner currently offers. The latter has a serious long-term impact on the level of trust that partners have in you, so this is not recommended. A reason for moving right is when features in the long tail become a must-have for most of the customers. You might want to secure that part of the solution by acquiring the partner.

<h2>Moving from a product to a platform company</h2>
The product long tail can be used to your advantage.

Moving left makes your own feature set smaller compared to the features provided by partners, while moving right makes your features set larger.

Moving left will make your development team focus on APIs for partners, while moving right has emphasis on UIs for customers only.

Moving left results in a platform company, while moving right results in a product company.

Before you can become a platform company, however, you need to first build the product with a customer base large enough to attract partners. With these partners you get huge leverage in solution development with a limited development team; you can deliver many solutions for customers.
