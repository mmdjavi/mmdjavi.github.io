---
layout: essay
type: essay
title: "Checkpoint Assignment #3"
# All dates must be YYYY-MM-DD format!
date: 2023-04-27
published: true
labels:
  - Assignment #3
  - Checkpoint
---
*The following below is a checkpoint in my progress for Assignment #3*

#### 1. Show what each page will look like. The pages do not have to be “functional” but the design should clear.

[Screencast Presentation](https://www.youtube.com/watch?v=gdVXj2aBA_Y) This is a link to my presentation which explains my plans for each page as well as how I will utilize sessions and cookies for Assignment #3.

#### 2. Describe your design for your site’s shopping cart. That is, will it be a separate page that the user can view and edit, or will it be integrated into the product pages? If so, describe in detail how this will work on your site. Provide several examples of using the cart.

For my site, I plan on displaying the user's shopping cart on a separate page through a tab on the right side of the navigation bar. Every page the user visits, they will have access to the cart regardless if they logged in or added any quantities. My shopping cart will allow users to make edits such as deleting a product or all products before checking out. I will also include buttons between the quantities box so that the user can increase or decrease the amount of products they want. This process will use sessions to send the user's purchases back to the server. Once the purchase is processed, the quantities of the respective products will decrease. Sessions will also ensure that the user is logged in by checking their status once they click the checkout/purchase button on the shopping cart page. This will also be helpful because server can retrieve the user's quantities and display the total number of products in the cart by the shopping cart on the navigation bar. 

#### 3. Explain specifically how you will use sessions to manage your shopping cart. In particular, what shopping cart data will be stored in the session, what data format will be used (NOT what data type, but the format like with the data format used for your registration data). Use code examples showing what data structures (such as arrays and their objects) you will use to manage the shopping cart data and how they will be used in a session.

In terms of managing my shopping cart data, I will sessions and more specifically, arrays and objects to keep track of the user's purchases. For example, on the server side I can request the session which has the user's product purchases in the cart: 

request.session\['products'] = \[{"name": "Chocolate Chip Cookie", "price": 1.25, "user_quantity": 8}];

With this, I can easily call the user's number of quantities to find the total quantity purchased for each product which will help with updating my products.json file. I can call "user_quantity" and subtract that amount to the quantities_available in my json file. I can also add the total quantities by calling "user_quantity" and display the total number of products in the shopping cart on the navigation bar. 

#### 4. How will you avoid access to your application when the user has not logged in or registered? What are the particular security concerns you must address?

Some security concerns I need to address are to ensure users are unable to access other user's data which can be avoided with the use of cookies. This is why the website will require users to login or register before completing their purchase despite being able to edit the shopping cart. Cookies can help with this as the user's login status does not have to be permanent but can remain within the timeframe of the user's session. Since cookies are not entirely secure and can be manipulated as it is on the client side, using cookies to check the user's status should be alright. Another way I can prevent this is setting a timer. Once a certain amount of time has passed and there is no activity, then the website will automatically end the user's session and log them out.

#### 5. Upon a successful login, how do you provide personalization in your UI? Explain how you did or will do this (paste code if necessary)

As discussed in the video, I plan on using cookies to determine if a user logged in successfully. If they did, I would be able to pull data such as the user's username and display their name with a "Welcome [username] back!" in the navigation bar. I can also personalize the invoice where it will also incorporate the user's information such as name and email address. These will be used to send the invoice to the user. 

#### 6. If you are working with partners, how will you split up the work in your team so that you are working in parallel as effectively as possible? That is, who is doing what and when?

I am working on Assignment #3 by myself.

#### 7. How are you approaching Assignment 3 differently than Assignment 2?

In terms of approach, Assignment 3 is just as challenge maybe even more than Assignment 2. I am on the lookout to determine if I have to start from scratch but for now I think what makes Assignment 3 a bit different is how I have to consider the user's experience as I write the code. I need to make sure the user has access to all my web pages while keeping their data secure. There are alot more validations to consider and UI changes to be made. I also have to keep track of where the user is and how they will be moving around each web page. This is why having an outline really helps to understand how the user will navigate around my website.
