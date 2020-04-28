---
title: 'Shop the Look'
subtitle: 'Connecting inspiration to action'
date: 2018-06-30 00:00:00
featured_image: '/images/stela.gif'
clickthrough: 'true'
---

![](/images/stela.gif)

#### Shopping Leader

I helped lead the company-wide shopping initiative to make Pinterest more actionable. Starting my work on shopping in 2018, I have been involved in almost every shopping feature that has been launched for the last two years.[^1][^2] More recently we had a huge milestone where we launched the ability to shop from every major recommendation surface on Pinterest.[^3] However, over the course of my 2.5 years contributing to shopping on Pinterest, one project stands out: Shop the Look. 

> "With Shop the Look Pins, people can find and buy products within fashion and home décor Pins, making it easy to bring inspiration to life."[^4]

<div class="gallery" data-columns="1">
	<img src="/images/stl.jpg">
	<img src="/images/stl2.jpg">
	<img src="/images/stl3.jpg">
</div>



#### Shop the Look - Manual Tagging
We launched Shop The Look as a way to help Pinners get to the products they love faster, and for brands to put customers on a path to purchase. 

The original product was human-curated pins that were manually tagged. The first step was a series of upfront costs to internally curate. We then built out an API to ingest tagged pins in bulk from approved third-party platform partners like curulate and shopstyle. This did not result in the scale we were looking for, so ultimately we decided to pursue a GA tagging tool, where any Pinner could tag images they own. This also aligned with the company's long-term strategy of focusing on user-generated content.[^5]

#### Shop the Look - Automatic Tagging
Ultimately, in order to scale coverage and increase the value for Pinners, we decided to automate tagging. At a high level there are 3 steps: (1) using our in-house object detection, we detect objects and their taxonomy labels within a scene image, (2) we restrict to only pins that are purchasable and within the same taxonomy label, and (3) we use an embedding model to find the nearest neighbors for recommendations. So as an example, we see a scene of a living room with multiple pieces of furniture, we detect all the bounding boxes and taxonomy labels like “couch” within that image, we then restrict all results to purchasable couches and finally find visually similar couches as recommendations.[^6]

The launch of this feature increased our Shop The Look Pin coverage by 22.5x!


#### Shop the Look - User Experience
One of the primary motivations of increasing coverage, was low comprehension of the feature. In addition to low coverage, these new pins suffered from the "cold start" recommendation problem and were getting proportionally lower distribution. In addition to simply covering more pins, we decided to tackle this from a frontend perspective and make the feature more discoverable and easy-to-use. We experimented with highlighting the tagged products beneath the image, animating the dots, moving the content forward in the funnel (e.g. moving the products one level up into the grid, in addition to the landing page). As we increased coverage and discoverability of the feature, we saw both engagement rates and volumes increase. This result is often hard to achieve at Pinterest due to diminishing returns and trading off quality for quantity. 

However, as we began to make this feature more pervasive, creators whose content was being automatically tagged with products from other brands, were starting to notice more and became unhappy. Pinterest has 3 distinct sets of users: Pinners, Creators, and Advertisers. This problem came down to trading off user satisfaction between the former two user types: Pinners and Creators. It was clear that Creators were upset, but as we dug deeper into user research, it became clear that not all the changes were positive for the Pinner either. Pinners had high expectations for dots to be exact matches and highly curated, as well as just feeling frustrated that viewing the image (the primary intent of Pinners) was becoming more difficult as we obfuscated it with dots. As a result of these learnings, we carefully balanced the business strategy, Pinner needs, and Creator satisfaction to end up with a feature that is non-obtrusive, highly discoverable, and intuitive. 


## Pretty cool, huh?

For more, find all the publications related to this feature below!

[^1]: 2018 - [New ways to shop with Pinterest](https://newsroom.pinterest.com/en/post/new-ways-to-shop-with-pinterest-0)
[^2]: 2019 - [More ways to shop your favorite brands on Pinterest](https://newsroom.pinterest.com/en/post/summer-shopping)
[^3]: 2020 - [New ways to shop on Pinterest](https://newsroom.pinterest.com/en/post/new-ways-to-shop-on-pinterest-discover-retailers-of-all-sizes)
[^4]: [Shop the Look Pins](https://business.pinterest.com/en-gb/shop-the-look-pins)
[^5]: [Shop the Look - Engineering Blog](https://medium.com/pinterest-engineering/engineering-shop-the-look-on-pinterest-45bdfa7a8d03)
[^6]: [Automating Shop the Look - Engineering Blog](https://medium.com/pinterest-engineering/automating-shop-the-look-on-pinterest-a17aeff0eae2)
