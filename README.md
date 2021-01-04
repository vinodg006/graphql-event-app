# Event Management App

A Full Stack web application built with MERN + GraphQL.

With this application you can view, book, create, cancel events . You can visualize the data using table in the front end or chart.


This application uses ExpressJS GraphQL framework(express-graphql) for the backend REST APIs (authenticated) and ReactJS for front-end views. The Data is stored with NoSQL database using MongoDB/mongoose.

## Glimpse of UI

![GIF](../master/screenshots/graphql-event-app-demo.gif)

**Login:**
![Screenshot](../master/screenshots/Login.png)

**Register:**
![Screenshot](../master/screenshots/Register.png)

**Dashboard/Events:**
![Screenshot](../master/screenshots/Dashboard.png)

**Create Event:**
![Screenshot](../master/screenshots/AddEvent.png)

**Book Event:**
![Screenshot](../master/screenshots/BookEvent.png)

**Bookings(Tab view):**
![Screenshot](../master/screenshots/Bookings.png)

**Bookings(Chart view):**
![Screenshot](../master/screenshots/Charts.png)

## Installation

Use npm to install graphql-event-app.

**Installing dependencies:**

    npm install && npm run client-install

**Running the server:**

    npm start

**Running the client:**

    npm run client

**Other Environment Variables:**

MONGO_USER : Database admin username.

MONGO_PASSWORD : Database admin password. 

MONGO_DB : Database name.


## Folder Structure

```

    |-- app.js (Server Code - mongoConn, graphql route def)
    |-- graphql
        |-- resolvers
        |-- schema
    |-- models (Models for collection documents)
    |-- middleware (Authenticate private routes)
    |-- heplers (Utility functions)
    |-- package.json
    |-- client (React App)
```

## Design Decisions

```bash

Pages: Login, Register, Events, Bookings

Login Page - Enter email, password. Hit Submit

Register Page - Enter  email, password. Hit Submit

Home Page: 

- Home page is loaded with list of events and bookings, logout in the navbar.

- Page displays list of events (with date, event name, price and description ) for the 
  logged in user.

- User can create,book and cancel events.
  - To add event, click Create Event button, it will open a 
    popup with form fields - Title, Price, Dtae and Description. Enter the details and hit
    Confirm Button.

```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
