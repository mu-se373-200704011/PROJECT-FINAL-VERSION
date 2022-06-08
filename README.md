**System Architecture Document**

**Problem Definition:**

As a developer, who is working remotely I always needed such a place where I can look for places to work at. There is such apps with similar usage and features but they are not specifically listing places to work. So, I wanted to create an app that suits those needs.

**So the problems to be solved by this application are:**

- Being able to search for places
- Being able to create a personal bookmarked list of shops
- Be able to add comments to those shops
- Be able to read comments of other users of those shops

**SYSTEM ARCHITECTURE**

**Functions**  **&amp;**  **Endpoints**

**Client:**

For client side, I&#39;ve developed an Ionic application within the use of React for UI purposes. This application is getting interacted with the server&#39;s Restful API to manage all the operations made by the user. Since it&#39;s a cross-compile framework, it is possible to build to both of the platforms; Android &amp; iOS

- User can create their account
- User can log in their account
- User can preview all the shops in the DB
- User can like or discard by swipe those shops
- User can create a list of saved shops by swiping right
- User can log out

**Server:**

On the server side, I created a web app that handles required CRUD operations in between end user to logic behind it. This project is developed on Flask micro-framework and for storage, I used MySQL. I tried to make similar-to MVC architecture on this web app. Whole deployment procedure is automated and running on Heroku. This side of the project also responsible for admin management. Adding shops to the DB and user permissions are handled on this [panel](http://work-n-travel-coffees.herokuapp.com/admin) **.**

- Login and authorize users by Bearer token JWT
- Register user
- Return list of shops
- Return list of comments added to this shop
- Manage session management, expiration of auth tokens
- Manage DB connections
- Manage DB changes, migrations

- All endpoints can be found at [swagger docs](https://work-n-travel-coffees.herokuapp.com/apidocs/)

**MODULES AND APIs**

**Client:**

- **react** => javascript framework
- **react-router** => navigate between pages
- **ionic-react** => some ionic components
- **Storage** => LocalStorage on mobile devices
- **axios** => for HTTP requests
- **TinderCard** => Swipe animation
- **react-router-dom** => for routing in between pages/components

**API:**

- **Flask**
- **flask\_login, PyJWT** => authentication
- **Pymysql, SQLAlchemy** => MySQL connection and management
- **BE**  **API deployed at** [**http://work-n-travel-coffees.herokuapp.com/**](http://work-n-travel-coffees.herokuapp.com/)

**Pages:**

- **Settings** (unprotected)
  - Register Page
<img src="/assets/images/register_log_in.png" width="200" />
  - Login Page
<img src="/assets/images/register_log_in.png" width="200" />
  - LogOut page
<img src="/assets/images/log_out.png" width="200" />


- **Home** (Protected)
- **List** (Protected)

**Database:**
<img src="/assets/images/db.png" width="200" />

Architecture Overview

**For client side**
<img src="/assets/images/c_arch.png" width="200" />

**For backend side**
<img src="/assets/images/b_arch.png" width="200" />
