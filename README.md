
# Tour Destinations

This full stack web application is specially designed for persons who love travelling and going on tour vacations. This API is based on MVC Architecture which follows REST philosophy and performs CRUD operations .

This app can be found at https://tour-destinations-dilli.onrender.com/ . The Official documentation of the API for this app can be found at https://documenter.getpostman.com/view/23609125/2s8ZDR8mGA .
## API Reference

#### Tour

```http
  GET https://tour-destinations-dilli.onrender.com/api/v1/tours

```

| Method | URL     | Description                |
| :-------- | :------- | :------------------------- |
| `GET` | `{{URL}}/api/v1/tours` | This returns all tour destinations. |
| `GET` | `{{URL}}api/v1/tours/?difficulty=easy&duration[gte]=5` |**Filtering** This will return all the tours with a difficulty of easy and duration greater than or equal to 5 |
| `GET` | `{{URL}}api/v1/tours/?sort=-price,ratingsAverage` |**Sorting** his will return all tours sorted by the largest price, and if there's a tie it'll display the tours with a lower ratingsAverage first. |
| `GET` | `{{URL}}/api/v1/tours/5ffd4710732be83aec3bce14` | Simply add the tour id to the GET all tours route to get information about a single tour. |
| `GET` | `{{URL}}/v1/tours/top-5-cheap` | This end point has been designed to get the 'top 5' tours that has been pre customized using 'Aggregation Pipeline'. |
| `GET` | `{{URL}}/api/v1/tours/tour-stats` | Get tour stats based on their difficulty, like the average rating of all easy tours. |
| `POST` | `{{URL}}/api/v1/tours` | Create a new tour by puttting Required field in body . |
| `POST` | `{{URL}}/api/v1/tours/60043fea1923ad28a88eee0d` | Add the id of the tour you want to update and pass the new data in the body (select 'raw' and 'JSON' in Postman). |
| `POST` | `{{URL}}/api/v1/tours/5c88fa8cf4afda39709c295a` | Add the id of the tour that you wish to delete. Expect a 204 No Content status code back and no data. |


#### Authentication

```http
  POST https://tour-destinations-dilli.onrender.com/api/v1/users/

```

| Method | URL     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `POST`      | `{{URL}}/api/v1/users/signup` | **SIGNUP** Sign up providing your name, email, and password. You can set your profile picture later.|
| `POST`      | `{{URL}}/api/v1/users/login` | **LOGIN** Login using your email and password. Your session will last 5 days, after that you'll have to login again.|



## Main Tools And Technologies Used:

- HTML (Create the structure and content of the web pages).
- CSS (Styling of the web pages).
- JAVASCRIPT (Interactivity, as well as making requests to the API from the client-side).
- NODE (Run JavaScript code on the server-side).
- EXPRESS (Node framework, meant to simplify the process of building complex server-side applications).
- MONGODB (Database for data persistence).
- MONGOOSE (Interacting with mongodb).
- JSON WEB TOKEN (Authenticating users).
- BOOTSTRAP (Designing static file ).



## Setting Up Your Local Environment

If you wish to play around with the code base in your local environment, do the following

```bash
  * Clone this repo to your local machine.
* Using the terminal, navigate to the cloned repo.
* Install all the neccessary dependencies, as stipulated in the package.json file.
* If you don't already have one, set up accounts with: MONGODB, POSTMAN ,EXPRESS. Please ensure to have at least basic knowledge of how these services work.
* In your .env file, set environment variables for the following:
    * DATABASE=your mongodb database url
    * DATABASE_PASSWORD=your mongodb password

    * SECRET=your json web token secret
    * JWT_EXPIRES_IN=90d
    * JWT_COOKIE_EXPIRES_IN=90

* Start the server.
- $npm init
- $npm Install
- $npm start /node server.js 
* Your app should be running just fine.
```

![ss1](https://user-images.githubusercontent.com/92309333/212540455-0bbcbf27-9e59-4978-979a-971764182465.png)


## Contributing :

Contributions are always welcome !This app is actually quite more complex so you can have brief overview by visiting official documentation of this API.
 Nevertheless, this summary is enough to help you understand the major features of the app. You are welcome to make improvements on the app. Please use the link specified at the beginning of the document to preview the app.



