---
layout: article
title: "Customize Your Ads"
description: "The best ads improve user experience; format ads so they don't look out of place on your site. While the actual ad content comes from advertisers, you have control over the content type, color, size, and placement of those ads."
introduction: "The best ads improve user experience; format ads so they don't look out of place on your site. While the actual ad content comes from advertisers, you have control over the content type, color, size, and placement of those ads."
article:
  written_on: 2014-07-17
  updated_on: 2014-07-17
  order: 3
id: customize-ads
collection: ad-monetization
key-takeaways:
  tldr: 
    - Use Responsive Ad Units for all inventory.
    - Look for opportunities to integrate ads throughout the content to avoid ad blindness;
    - Never place ads where they might interfere with a user's intended experience on your site; ensure ads above the fold don't push content below it.
    - Maximize revenue by allowing text and display images to compete for your ad space.
    - Style your ads so they don't look out of place on your site; choose text styles that blend, compliment, or contrast your site.
notes:
  targeting:
    - Ads are targeted based on overall site content, not keywords or categories. If you'd like to display ads related to specific topics, include complete sentences and paragraphs about these topics.
  testing:
    - While smart sizing should automatically display ads in the best size based on the user's device, you should always test your ads on different devices and screens to make sure that the responsive behavior is working correctly.
  images:
    - Advertisers have full control over how their display ads look. You can influence the types of display ads that appear on your site using ad placement and sizing, but you can't actually control the image content.
---

{% wrap content %}

<style type="text/css">
  img.center {
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
</style>

{% include modules/toc.liquid %}

{% include modules/takeaway.liquid list=page.key-takeaways.tldr %}

## Size ads in relation to the user's device

The simplest and most effective way to size your ads so that they respond
to a user's device is to
[create responsive ad units]({{site.baseurl}}/monetization/ad-monetization/include-ads.html#create-ad-units).

To make your code simpler and save you time and effort,
the responsive ad code automatically adapts the ad unit size to your page layout.
The code calculates the required size dynamically based on the width of the ad unit’s parent container,
then determines what's the best standard height to go with that width:

*** Todo: contacted PM for details on algorithm that controls smart sizing;
will complete this table once I hear back.***

<table class="table-2 tc-heavyright">
  <colgroup>
    <col span="1" />
    <col span="1" />
  </colgroup>
  <thead>
    <tr>
      <th data-th="size">Parent container width</th>
      <th data-th="behavior">Ad size served</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td data-th="command">Todo</td>
      <td data-th="alias">Todo</td>
    </tr>
    <tr>
      <td data-th="command">Todo</td>
      <td data-th="alias">Todo</td>
    </tr>
    <tr>
      <td data-th="command">Todo</td>
      <td data-th="alias">Todo</td>
    </tr>
  </tbody>
</table>

{% include modules/remember.liquid title="Important" list=page.notes.testing %}

## What if responsive sizing isn't enough?

If the smart sizing isn't exactly what you want in your site,
you can switch to advanced mode and override smart sizing
in your responsive ad unit code
(see [Advanced features in this help topic](https://support.google.com/adsense/answer/3543893?hl=en&ref_topic=3641113)).

For example,
you can control the exact sizing of ads using
[media queries]({{site.baseurl}}/layouts/rwd-fundamentals/use-media-queries.html):

1. Follow the instructions to [create a responsive ad unit]({{site.baseurl}}/monetization/ad-monetization/include-ads.html#create-ad-units).
2. In the Ad code box,
select the <strong>Advanced (code modification required) mode
from the Mode drop-down.
3. Modify the ad code to set the exact sizes of your ads based on the user's device:

{% highlight html %}
<style type="text/css">
.adslot_1 { width: 320px; height: 50px; }
@media (min-width:500px) { .adslot_1 { width: 468px; height: 60px; } }
@media (min-width:800px) { .adslot_1 { width: 728px; height: 90px; } }
</style>
<ins class="adsbygoogle adslot_1"
    style="display:inline-block;"
    data-ad-client="ca-pub-1234"
    data-ad-slot="5678"></ins>
<script async src="//pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>
<script>(adsbygoogle = window.adsbygoogle || []).push({});</script>
{% endhighlight %}

If you're considering overriding smart sizing,
the Google AdSense [Guide to ad sizes](https://support.google.com/adsense/answer/6002621?hl=en&ref_topic=1307421)
is a great resource for choosing the best ad sizes.

## Place ads where users benefit the most

When it comes to deciding where to place ads on your site,
and how many ads to include, always put the user first
(see also these
[best practices for ads placement](https://support.google.com/adsense/answer/1282097?ref_topic=3001646&rd=1)):

* Use ads to augment site content; not the other way around.
* Always follow the [Google AdSense program policies](https://support.google.com/adsense/answer/48182?hl=en()). Pages with excessive ads, ads that push the content down below the fold, ads clustered together that dominate the viewable space or ads without clear labeling are all against ad policies.
* Avoid adding too many units which distract users from content.
* Ensure ads provide value to users. If you have ad units that generate significantly less revenue or drive less clicks or views, it’s likely they are not providing value to users.
* Maintain a balance between ads and content. Avoid adding too many units which distract users from content.

Sample placement options for mobile ads:

<img src="images/mobile_ads_placement.png" class="center" alt="Sample mobile image ad">

## Maximize bidding potential

The higher the competition, or ‘auction pressure’,
the more the advertiser will pay to be viewed and clicked on your site.
To maximize your bidding potential:

* Allow [text](https://support.google.com/adsense/answer/185665?hl=en&ref_topic=29561)
and [display ads](https://support.google.com/adsense/answer/185666?hl=en&ref_topic=29561)
for each ad unit. Many advertisers include images in their ads;
if you exclude display ads, you lose out on more advertisers bidding for your ad space.
* [Maximize ad space](https://support.google.com/adsense/answer/17958?hl=en&ref_topic=3001714)
by including more than one ad unit in your site.
* Use ad sizes that are popular with advertisers, for example, 300px by 250px
(see also the [Guide to ad sizes](https://support.google.com/adsense/answer/6002621?hl=en&rd=1)).
* Place ads near your content, but don't let the ads get in the way of that content (see also
[Best practices for ads placement](https://support.google.com/adsense/answer/1282097?hl=en&ref_topic=3001646)). 

## Choose text styles that compliment your site

The [most successful ad styles](https://support.google.com/adsense/answer/17957)
blend or contrast with your site's styles.
Create combinations of colors and fonts that compliment your site
and bring you the best revenue opportunies. 

### What can you customize?

You have full control over the following styles applied to text ads:

* Border color
* Background color
* Text font family and font size
* Default text color
* Text color specific for the ad title
* Text color specific for URLs

{% include modules/remember.liquid title="Note" list=page.notes.images %}

### How to apply styles

Google AdSense comes with
<a href="https://support.google.com/adsense/answer/6002585">predefined ad styles<a/>.
Use these predefined styles as is, tweak predefined styles, or create a style from scratch.

Todo: flesh out these instructions.

<img src="images/customize.png" class="center" alt="Ads styles customization window">

{% endwrap %}
