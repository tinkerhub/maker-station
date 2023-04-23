# Rest (Representational State Transfer) API
#### What is API (API) ?

API stands for Application Programming Interface. It's a set of protocols and tools that allow different software systems to communicate with each other.
In other words, it's like a messenger that carries requests and responses between different applications.

### Simple explanation
An API is like a waiter who takes your order (request) and brings you food (response) from the kitchen. It helps different apps talk to each other and work together.

### Expanded explanation example
An API is like a messenger that carries requests and responses between different applications, just like a waiter carries orders to the kitchen and brings food back to the table. It helps apps talk to each other and work together, allowing them to access and use the resources and functionalities of a server. In simpler terms, an API enables different apps to share and use each other's services, making it easier to build complex software systems.


# What is an RestAPI
REST is a way for computers to talk to each other over the internet. It uses certain rules, called constraints, to make sure everyone can understand each other.

In HTTP there are four methods that are commonly used in a REST-based Architecture 
**GET**,**POST**,**PUT** and **DELETE**. 
These correspond to create, read, update, and delete (or CRUD) operations respectively.
There are other methods which are less frequently used like **PATCH**,**OPTIONS** and **HEAD**.  

### HTTP METHODS (Four main ways computers can talk to each other using REST): 
1. **GET** (retrieve a record)
2. **POST** (create a record)
3. **PUT** (update a record)
4. **DELETE** (delete a record)

One of the main features of a RESTful API is that it is **"stateless"**, which means that the server does not keep track of any information about the client's previous requests.

### Simple explanation
Each time the client sends a request to the server, it includes all the information needed for the server to process the request and send back a response. The server doesn't need to remember anything about the client's previous requests.

### Expanded explanation with examples

Let's say you and your friends are playing a game. When you make a move in the game, you tell your friend what you want to do, and your friend tells you what happens as a result of your move.

Now imagine that you and your friends are playing this game with a really big group of people. You all agree that you're only going to talk to each other using a special language, kind of like a secret code. This makes it easier for everyone to understand what's going on.

But there's one more rule: after each move, everyone forgets everything that happened in the game so far. That means that you can't rely on your friends to remember anything about your previous moves. You have to explain what you want to do every time you make a move, just like it's the first time you're playing the game.

This might seem like a strange rule, but it makes it easier to play the game with lots of people at once. Nobody has to remember everything that's happened so far and everyone can just focus on what's happening right now.

This is kind of like how REST works. It's a way for computers to talk to each other using a special language, and they agree to forget everything that's happened between requests. This makes it easier to handle lots of requests at once without getting confused.
This approach makes the API more scalable and reliable, because the server can handle a large number of requests from many different clients without getting confused or overwhelmed.
 
# How it works (explained with real life scenario) 
Imagine that you want to use the Zomato app to order food.
You would open the app, browse the menu, and select the items you want to order.
Once you've placed your order, the app sends a request to the Zomato server, 
which processes the request and sends a response back to the app with the details of your order.

In this scenario, Zomato is using a REST API to communicate between the app and the server. REST stands for Representational State Transfer and is a type of API that uses HTTP requests to get or send data. It follows a set of architectural principles that make it easy to scale, modify, and maintain.

**Advantages:**

**Flexibility:** REST APIs can be used with any programming language and are platform-independent, which means they can be used on any device or operating system.

**Scalability:** REST APIs can handle a large number of requests and are easy to scale up or down as needed.

**Easy to develop:** REST APIs follow a set of standard rules, which makes them easy to develop and integrate with other apps.

**Caching:** REST APIs can use caching to improve performance and reduce server load, which can improve the user experience.

**Security:** REST APIs can use secure authentication methods such as OAuth to
ensure that only authorized users can access the data.

In simpler terms,
a REST API is a type of API that uses HTTP requests to communicate between an 
app and a server. It's easy to use and can handle a lot of requests. REST APIs 
follow standard rules that make them flexible, scalable, and secure.

## Example of API's

Before knowing example you should know the terms like **Url**, **Domain** 
& **Endpoint**

**URL :** https://www.zomato.com/

In this example, the URL is the complete web address used to access the homepage of the **zomato.com** website.

**Domain :** www.zomato.com

The domain is the main part of the web address that identifies the website or server that hosts the web application. In this example, the domain is www.zomato.com which is the website that hosts the zomato.com web application.

**Endpoint :** */search*

The endpoint is the specific URL that represents a resource or functionality within the web application. In this example, the endpoint is **/search** which is a page within the zomato.com application that allows users to search for restaurants in their area.

To access this endpoint, a user could navigate to the following URL:

https://www.zomato.com/search

If the request is successful, the zomato.com application would display a page where the user can search for restaurants in their area.

Overall, the URL, domain, and endpoint are important components of a web address and are used to locate and access specific resources and functionality within web applications.


# Search Restuarant API (API name)

## ``GET`` ``/search``

### Request Structure

#### Header :-
| KEY | VALUE | TYPE | DESC |
| --- | ----- | ---- | ---- |
| Content-Type | application/json | string | Set the content type of the request body |
| User-Agent | Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/77.0.3865.90 Safari/537.36 | string | Identifies the client accessing the server |


#### Body:-
| KEY | VALUE | TYPE | DESC |
| --- | ----- | ---- | ---- |
| location | Kozhikode | string | Required. The name or address of the location to search for restaurants |
| sort | rating | string | Optional. The sort order to use for the search results. Possible values: cost, rating, real_distance, popularity |

### Response Structure


```json
{
  "results_found": 3,
  "hotels": [
    {
      "id": "1",
      "name": "Nahdi Kuzhi Mandi",
      "location": {
        "address_line_1": "123 Beach Road",
        "address_line_2": "",
        "city": "Kozhikode",
        "state": "KL",
        "pin_code": "673001"
      },
      "phone_numbers": {
        "main": "+91 495 1234567",
        "fax": "+91 495 1234568"
      }
    },
    {
      "id": "2",
      "name": "Rahmath Hotel",
      "location": {
        "address_line_1": "Aravind Ghosh Rd, near Mathrubhumi Office, 
                            Mananchira, Kozhikode, Kerala 673001",
        "address_line_2": "",
        "city": "Kozhikode",
        "state": "KL",
        "pin_code": "673002"
      },
      "phone_numbers": {
        "main": "+91 495 2345678",
        "fax": "+91 495 2345679"
      }
    },
    {
      "id": "3",
      "name": "Edele Hotel",
      "location": {
        "address_line_1": "Near Mishkal Mosque, Kuttichira",
        "address_line_2": "",
        "city": "Kozhikode",
        "state": "KL",
        "pin_code": "673003"
      },
      "phone_numbers": {
        "main": "+91 495 3456789",
        "fax": ""
      }
    }
  ]
}

```

## The resources available for implementing REST APIs in different frameworks
- [Django REST framework](DjangoRestFramework.md)
- [FastAPI](FAST%20API.md)
