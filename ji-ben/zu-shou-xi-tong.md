# 租售系统

Areas can either be setup for rental via the menu or using a sign.

## Menu

1. Place a sign in the sub area that you want to setup to be rented or sold.
2. Execute `/lands menu here` while standing in the area
3. Click on the setup rental item
4. Set all values and confirm

## Rent Sign

#### Rent sign setup:

![Rent sign setup](https://imgur.com/am5U7Sp.jpg)

#### Explanation

Parameters surrounded by `[]` are optional. Parameters surrounded by `<>` are required.

* \[area]: This parameter is only needed if the sign is placed outside the area.
* `<interval>`: The tenant can extend their rental by `<interval>`. Time units: d (days), h (hours) and m (minutes). Default is `d`. Example: 15d = 15 days
* `<max>`: Is the max. duration of the rental.
* `<cost>`: Defines the cost per `<interval>`.

You can only set sub areas for rent. The default area can only be set for sale (= selling the whole land; more information below)

**Example:**

![](https://imgur.com/IX3XwlJ.jpg)

#### When the Sign has been placed

* The rent sign is setup and players can now access it.
  * To rent this area, just click on the sign.
  * To add more time to your rental, just click again on the sign.
* Cancel rental
  * Tenants can use /lands rent cancel to cancel their rental while standing inside the area.
* Remove the rental
  * As the area owner you can either remove the sign or execute /lands rent remove while standing inside the area.

## Sell Sign

#### Sell sign setup

Sell signs can be placed in sub areas and in the default area (= selling the whole land)\
![Sell sign setup](https://imgur.com/Qy68zNh.jpg)

#### Explanation

Parameters surrounded by `[]` are optional. Parameters surrounded by `<>` are required.

* \[area]: This parameter is only needed if the sign is placed outside the area.
* `<cost>`: Defines the total cost.

**Example**

![Sell sign result](https://imgur.com/9uRyayN.jpg)

#### When the Sign has been placed

[Click](https://github.com/Angeschossen/Lands/wiki/Rent-System/\_edit#when-the-sign-has-been-placed)

## Browse Listings

Use `/lands rent list` to view all areas and lands that can be rented or bought. There you can also filter and sort these offers.
