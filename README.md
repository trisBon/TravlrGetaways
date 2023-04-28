# Architecture
Compare and contrast the types of frontend development you used in your full stack project, including Express HTML, JavaScript, and the single-page application (SPA).
Why did the backend use a NoSQL MongoDB database?

I created an Express HTML customer facing website and an Angular single-page application for the company's admin site. The Express website responds to user button clicks by serving a new HTML template for all of the site functions. For the Angular app, HTML is only loaded at start of the application, and only data is passed back and forth between the app and the server. A JavaScript API was used to handle HTTP requests for the admin site. A NoSQL database was used for the app to support flexibility, scalability, and for its compatability with Express, Angular, and JavaScript. 


# Functionality
How is JSON different from Javascript and how does JSON tie together the frontend and backend development pieces?
Provide instances in the full stack process when you refactored code to improve functionality and efficiencies, and name the benefits that come from reusable user interface (UI) components.

JSON templates were used to format data in both the front and backend of the program. Both JSON and JavaScript are used to store and transfer data, but JSON is text based, while JavaScript uses JavaScript Objects. 

JSON handle bars were used to replace the repeated lines of header and footer code in the Express app. The code was the same on each HTML page, so this helped significantly decrease the number of code lines. Specifically, the travel.hbs view decreased the HTML file from 119 lines to 36 lines of code. 

For the admin code I used JavaScript Objects to create app components that could be reused. The trip-card component is used inside of the trip service, and it creates a new trip card for each of the trips stored in the MongoDB database. Using a single html file, I was able to create the layout for each card, which meant having one file to reference. Adding functionality to the cards, like the edit and delete buttons, was as simple: all I had to do was add methods to the trip-card.component.ts file. Setting up this functionality took a decent amount of time, but simplified the process for editing the UI.

# Testing
Methods for request and retrieval necessitate various types of API testing of endpoints, in addition to the difficulties of testing with added layers of security. Explain your understanding of methods, endpoints, and security in a full stack application. 

The GET, POST, PUT, and DELETE methods used in my API I were created to support CRUD functionality in my application. I useed the CORS bootstrap to hanlde the access control handlers in app.js, and setup the method logic inside trip-data.service.ts. The code for registering the API endpoints is written in app_api>routes>index.js, and specifies where control is routed based on different user interactions. Security of the app is also set up in these same areas, and required the creation of additional components for login, home, and the navbar. Additional layers of security increase the complexity for testing. Testing can be done using a combination of PowerShell, and Chrome's browser inspection tool, or using a service like Postman. There are a numbner of interacting parts in the application, and the fact that errors can occur in any part of the project is what creates the added level of complexity. 

# Reflection
How has this course helped you in reaching your professional goals? What skills have you learned, developed, or mastered in this course to help you become a more marketable candidate in your career field?

My current professional goal is to be employed in my field, so it is too soon to say whether this course has helped or not. However, completing my degree is an essential step in completing my degree, so it definitely hasn't hurt. In taking this class, I learned the basics of building a full-stack application, and I gained familiarity with common software tools used in the industry. If having used something once in a limited capacity can be said to increase my "marketability", this course has certainly benefited me.
