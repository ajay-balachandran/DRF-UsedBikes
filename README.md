# DRF-UsedBikes

## How To Setup Project
1. Clone This Project git clone https://github.com/ajay-balachandran/DRF-UsedBikes.git <br/>
2. Go to Project Directory `cd DRF-UsedBikes`<br/>
3. Create a Virtual Environment `python -m venv venv`<br/>
4. Activate Virtual Environment on **linux and mac** `source venv/bin/activate`, on **windows** `venv\Scripts\activate`<br/>
5. Install Requirements Package `pip install -r requirements.txt`<br/>
6. Finally Run The Project `python manage.py runserver`<br/>

## Features Added:

    - JWT Authentication
    - API to create, retrieve, update, delete bike selling posts
    - API to add, retrive multiple images for a bike selling post
    - API to make offers to seller, list all offers of a spesific bike selling post
    - API to mark a bike selling post as sold
    - API to update offer price
    - API to accepting or cancel offers
    - etc.....
    - I will add more functionalities to this project in future, Currently only API's are developed, test it by using Postman, Thunderclient(VScode Extension) or other API testing tools
    
## API Documentation

| Url | Method | Description | Data | Authorization |
| --- | --- | --- | --- | --- |
| localhost:8000/token/ | POST | For generating Access and Refresh Tokens | Username, Password | Null |
| localhost:8000/token/refresh/ | POST | For generating access Token using a refresh token | Refresh Token | Null |
| localhost:8000/usedbikes/bikes/ | POST | For creating a new bike selling post | Required Bike Details | access token |
| localhost:8000/usedbikes/bikes/ | GET | For list all bikes | Null | Null |
| localhost:8000/usedbikes/bikes/{id}/ | GET | For retrieve details of specific a bike | Null | Null |
| localhost:8000/usedbikes/bikes/{id}/ | PUT | For updating details of a specific bike | Required Bike Details | access token |
| localhost:8000/usedbikes/bikes/{id}/ | DELETE | For deleting a specific bike | Null | access token |
| localhost:8000/usedbikes/bikes/{id}/add_images/ | POST | For adding images of a bike | Image | access token |
| localhost:8000/usedbikes/bikes/{id}/get_images/ | GET | For retrieve images of a specific bike | Null | Null |
| localhost:8000/usedbikes/bikes/{id}/make_offer/ | POST | For make an offer to seller | offer_price | access token |
| localhost:8000/usedbikes/bikes/{id}/offer_requests/ | GET | For list all offers of a specific bike | Null | access token |
| localhost:8000/usedbikes/bikes/{id}/mark_as_sold/ | POST | To mark a bike post as sold | Null | access token |
| localhost:8000/usedbikes/offers/ | GET | For list all offers created by login user | Null | access token |
| localhost:8000/usedbikes/offers/{id}/ | GET | For retrieve a specific offer created by login user | Null | access token |
| localhost:8000/usedbikes/offers/{id}/ | UPDATE | For update an offer price | offer_price | access token |
| localhost:8000/usedbikes/offers/{id}/ | DELETE | For delete an offer make by the logined user | Null | access token |
| localhost:8000/usedbikes/review_offer/{id}/ | GET | For retrieveing a specific offer request | Null | access token |
| localhost:8000/usedbikes/review_offer/{id}/accept_offer/ | POST | For accepting an offer request | Null | access token |
| localhost:8000/usedbikes/review_offer/{id}/cancel_offer/ | POST | For cancel an offer request | Null | access token |
| localhost:8000/usedbikes/sales/sold_bikes/ | GET | For list all sold bikes of logined user | Null | access token |
| localhost:8000/usedbikes/sales/bought_bikes/ | GET | For list all bikes bought by logined user | Null | access token |


   
### Tools & Technologies Used:

`python` `djangorestframework` `sqlite` `git & github`
