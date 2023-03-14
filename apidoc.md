//Page1 (search Page)

> List of city
 (GET) http://localhost:1009/location

 > List of restaurants 
 ( GET) http://localhost:1009/restaurants

> restaurants wrt city
(GET) http://localhost:1009/restaurants?stateId=4

>List of MealTypes
(GET) http://localhost:1009/mealTypes

//Page2 (listing Page)

Restaurants wrt meal
> (GET) http://localhost:1009/restaurants?mealId=4

> http://localhost:1009/restaurants?stateId=1&mealId=3

(GET) Restaurants wrt to meal + cuisine
http://localhost:1009/filter/2?cuisineId=4

> Restaurants sort wrt to meal+cost 
(GET) http://localhost:1009/filter/1?lcost=700&hcost=2000
 
 >Restaurants sort wrt to cost
 (GET) http://localhost:1009/filter/2?cuisineId=1&sort=-1

 Pagination
http://localhost:1009/filter/2?cuisineId=1&skip=2&limit=2

//Page3 (details Page)

> Restaurants Details
(GET) http://localhost:1009/details/6405d49965785f6a71c2b3cd
> Menu wrt restaurants
(GET) http://localhost:1009/menu/4

//Page4 (placeOrder Page)

> Menu details 
(POST) http://localhost:1009/menuItem
{"id":[2,32,4]}

> Place Order
(POST) http://localhost:1009/placeOrder

[
    {
        "_id": "640c5aef4b41eea356180e0e"
    },
    {
        "_id": "640c5af04b41eea356180e0f"
    },
    {
        "_id": "640c5af94b41eea356180e10"
    },
    {
        "_id": "640c5afb4b41eea356180e11"
    },
    {
        "_id": "640c5b024b41eea356180e12"
    },
    {
        "_id": "640c5b144b41eea356180e13"
    },
    {
        "_id": "640c5bc44b41eea356180e14",
        "orderId": 1,
        "name": "Jeffs",
        "email": "jeffs14@gmail.com",
        "address": "saturnring 03",
        "phone": 8995657570,
        "cost": 455,
        "menuItem": [
            34,
            67,
            40
        ]
    },
    {
        "_id": "640c68cd1ec89aae978f3cb1",
        "orderId": 1,
        "name": "Jeff",
        "email": "jeff14@gmail.com",
        "address": "saturn 03",
        "phone": 8995897570,
        "cost": 499,
        "menuItem": [
            56,
            32,
            48
        ]
    }
]

 
//Page5 (orderListing Page)

> List All Order Placed
(GET) http://localhost:1009/orders

> Order wrt email
(GET) http://localhost:1009/orders?email=anchal@gmail.com

> Delete Order
(Delete) http://localhost:1009/removeOrder

>Update Order

(PUT) http://localhost:1009/updateOrders