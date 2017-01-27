---
lang: en
layout: article_with_sidebar
updated_at: '2017-01-24 12:36 +0400'
identifier: ref_V0WJ7Tzu
title: Changing the checkout logos picture
order: 400
published: true
version: X-Cart 5.3.3
---
**Checkout logos** is the picture of the accepted payment methods or security certificates, which is generally shown at the checkout header section. It was introduced in X-Cart 5.3.3:

![checkout_logos_picture.png]({{site.baseurl}}/attachments/ref_V0WJ7Tzu/checkout_logos_picture.png)

You can customize this picture to show something else by doing these steps:

1.	Install and enable the [ThemeTweaker addon](https://market.x-cart.com/addons/theme-tweaker.html).

2.	Place the desired PNG picture by the path:
	
    `<X-Cart Dir>/skins/theme_tweaker/customer/images/checkout_logos.png`

That's it, the new picture will substitute the default one and will be shown to every customer. This modification will be saved during the upgrade. To revert changes simply delete the picture you've added.