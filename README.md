# Ads-System-and-Shopping-System
This project intends to build a shopping and ordering web application with Spring Framework and dispaly ads inside.

## Ads System
The ads system focus on creating ads, bidding ads and choosing the appropriate ads to display.

### functions
create ad (/CreateAd), create advertiser (/CreateAdvertiser), update bid (/UpdateBid), update budget (/UpdateBudget) and choose the right ad to display (/Ad).

We choose the right ad based on the CPC Bid and Quality Score.

### database
Table ad:

|  ad_id  |   bid    | image_url  | advertiser_id | ad_score|
|---------|----------|------------|---------------|---------|
| 1       | 5        | image_url  | 1             |  0.6    |

Table advertiser:

| advertiser_id   | name               | budget |
|-----------------|--------------------|--------|
| 1               | att                | 98.1996|

## Shopping system
The users can browse items, add to cart and checkout. The admin can post and delete items.

### functions
login, logout, register, add product, browse product, add to cart, checkout

### database
Database design:
<img width="626" alt="screen shot 2018-09-16 at 17 17 15" src="https://user-images.githubusercontent.com/40250261/45602505-6a27d200-b9d4-11e8-8d88-e9153f48b69a.png">

### realization
1. There are four packages under the main package onlineShop

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;a. model package

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Create models of the database using Hibernate. (refer to database design)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;b. dao package

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Define and realize actions to deal with database, for functions for cart, cart item, customer, product and sales order.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;c. service package

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Define and implement services we want to achieve. This package realize its function based on dao package.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;d. controller package

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Map urls and call related service in service package.

2. config files

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;a. ApplicationConfig

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Prepare for the application, like set properties for Hibernate.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;b. SecurityConfig

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Authenticate and authorize different rights for average user and admin.

3. webflow
checkout-flow.xml defines the flow from add cart to order to thank you customer.

## demo
demo link: https://drive.google.com/file/d/1fkDcTE1NvP6vTBIjWOulJZzWO-KYISAx/view
