# eCommerce Storefront Scraper
Crawler + Scraper to identify all items unavailable for purchase. 

PROBLEM: 

Magento2 observer is broken, so sold-out items remain active on the e-storefront. The styling and content on those products' pages are ambiguous, so customers are often unaware that the items is no longer available.

CONSTRAINTS:

(1) Retailer does not have access to/control over page styling or code. (Therefore, unable to conditionally trigger "Out of Stock" messages or disable page elements.)  

(2) Solution must work around the disabled Magento2 feature / not touch the Magento2 core (in other words, NOT a Magento2 extension). Instead, retailer needs a solution that operates independently of the Magento platform (like an executable script).

BACKGROUND: 

Small apparel company relies on Magento2 e-commerce platform to integrate with their brick-and-mortar point-of-sale system to dynamically reflect their fluctuating inventory of approximately 2,000 products, so that online and in-person customers see the same thing. However, Magento2's native "observer" feature (to detect, inactivate and redirect URLs for sold-out products) causes unintended side effects elsewhere, and had to be disabled. Further, Magento2's admin interface doesn't provide the tools needed to find all unavailable products. The only way to identify these items on the storefront is manually, and their page will render differently for different product types (either a $0.00 price, or the Add-To-Cart button will disappear). Therefore, the retailer's only option is to manually/visually inspect all 2,000 product pages several times a day -- realistically, this is impossible. Usually, these products come to the company's attention when users contact customer service. From the UX standpoint, customers do not know a product is out of stock. Instead, it appears to be an issue with the shopping cart. 

TL;DR:
Need to programmatically, comprehensively find any unavailable items before customers do (and spare customer service the call volume).  

Steps Taken:

Libraries used:
