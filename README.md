## LIVE DEMO :- <a href="https://quirky-allen-bbaed4.netlify.app/login">Nxt TretZ</a>

### E-Commerce Application
Make an Authentication Request to Login API</br>
Handle Login API Response</br>
On Login Success</br>
On Login Failure</br>
Store the JWT Token</br>


### In this assignment let's build a **Nxt Trendz** App with Authentication 

### Refer to image below:
** -- https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-authorisation-output-v2.gif -- **
<br/>
<div style="text-align: center;">
    <img src="https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-authorisation-output-v2.gif" alt="nxt-trendz-authorisation-desktop-output" style="max-width:90%;box-shadow:0 2.8px 2.2px rgba(0, 0, 0, 0.12)">
</div>
<br/>

#### Design Files

<details close>
<summary>Click to view the Design Files</summary>
<br>

- [Extra Small (Size < 576px), Small (Size >= 576px), and Medium (Size >= 768px) - Login](https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-authentication-sm-login-output-v2.png)
- [Extra Small (Size < 576px), Small (Size >= 576px), and Medium (Size >= 768px) - Login Error](https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-authentication-sm-login-error-output-v2.png)
- [Extra Small (Size < 576px) and Small (Size >= 576px) - Home](https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-authorisation-sm-home-output.png)
- [Extra Small (Size < 576px) and Small (Size >= 576px) - Products](https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-authorisation-sm-products-output.png)
- [Extra Small (Size < 576px) and Small (Size >= 576px) - Cart](https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-authorisation-sm-cart-output.png)

- [Large (Size >= 992px) and Extra Large (Size >= 1200px) - Login](https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-authentication-lg-login-output.png)
- [Medium (Size >= 768px), Large (Size >= 992px) and Extra Large (Size >= 1200px) - Home](https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-authentication-lg-home-output.png)
- [Medium (Size >= 768px), Large (Size >= 992px) and Extra Large (Size >= 1200px) - Products](https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-authorisation-lg-products-output.png)
- [Medium (Size >= 768px), Large (Size >= 992px) and Extra Large (Size >= 1200px) - Cart](https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-authorisation-lg-cart-output.png)
- [Medium (Size >= 768px), Large (Size >= 992px) and Extra Large (Size >= 1200px) - Not Found](https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-authentication-lg-not-found-output.png)

</details>

### Project Set Up Instructions

<details close>
<summary>Click to view the Set Up Instructions</summary>
<br>

- Download dependencies by running `npm install`
- Start up the app using `npm start`

</details>

### Project Completion Instructions

<details close>
<summary>Click to view the Functionality to be added</summary>
<br>

#### Add Functionality

The app must have the following functionalities

- When an unauthenticated user tries to access the `HomeRoute`, `ProductsRoute`
  or `CartRoute` then the page should be redirected to the `LoginRoute`.
- When an authenticated user tries to access the `HomeRoute`, `ProductsRoute` or
  `CartRoute` then the page should be navigated to the respective route.
- When an authenticated user tries to access the `LoginRoute` then the page
  should be redirected to the `HomeRoute`.
- When the Logout button is clicked then the page should be navigated to the
  `LoginRoute`.
- When an undefined path is provided in the URL then the page should navigate to
the `NotFoundRoute`
</details>

<details close>
<summary>Click to view the Example response</summary>
<br>

- Success response from the URL `https://apis.ccbp.in/login` will be

```json
{
  "jwt_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6InJhaHVsIiwicm9sZSI6IlBSSU1FX1VTRVIiLCJpYXQiOjE2MTk2Mjg2MTN9.nZDlFsnSWArLKKeF0QbmdVfLgzUbx1BGJsqa2kc_21Y"
}
```

- Failure response from the URL `https://apis.ccbp.in/login` for an invalid
  username will be

```json
{
  "status_code": 404,
  "error_msg": "Username is not found"
}
```

</details>

<details close>
<summary>Click to view the Implementation Files</summary>
<br>

- Your task is to complete the implementation of

  - `src/App.js`
  - `src/components/LoginForm/index.js`
  - `src/components/Header/index.js`
  - `src/components/Header/index.css`
  - `src/components/Products/index.js`
  - `src/components/Products/index.css`
  - `src/components/Cart/index.js`
  - `src/components/Cart/index.css`

</details>

#### Quick Tips

<details close>
<summary>Click to view Quick Tips</summary>
<br>

- The `onBlur` event listener is called when the element has lost the focus.
- You can use the below box-shadow CSS property to apply box-shadow effect to
  the containers,

  ```
    box-shadow: 0px 8px 40px rgba(7, 7, 7, 0.08);

  ```

- You can use the below cursor CSS property for buttons to set the type of mouse
  cursor, to show when the mouse pointer is over an element,

  ```
    cursor: pointer;
  ```

  <br/>
   <img src="https://assets.ccbp.in/frontend/content/react-js/cursor-pointer-img.png" alt="cursor pointer" style="width:100px" />

- You can use the below outline CSS property for buttons and input elements to
  remove the highlighting when the elements are clicked,

  ```
    outline: none;
  ```

</details>

> #### Important Note
>
> <details open>
> <summary>Click to view Important Note Points</summary>
> <br>
>
> - `HomeRoute` should consist of "/" in URL path
> - `LoginRoute` should consist of "/login" in URL path
> - `ProductsRoute` should consist of "/products" in URL path
> - `CartRoute` should consist of "/cart" in URL path
> - No need to use the `BrowserRouter` in `App.js` as we have already included
>   in `index.js`
> - Request body
>
>   ```
>   {
>     "username": "rahul",
>     "password": "rahul@2021"
>   }
>   ```
>
> - Valid credentials
>
>   ```
>    username: rahul
>    password: rahul@2021
>   ```
>
> - Access the error message for invalid requests with the key `error_msg`
> </details>

### Resources

<details close>
<summary>Data Fetch URLs</summary>
<br>

- `https://apis.ccbp.in/login`
</details>

<details close>
<summary>Image URLs</summary>
<br>

- [https://assets.ccbp.in/frontend/react-js/nxt-trendz-logo-img.png](https://assets.ccbp.in/frontend/react-js/nxt-trendz-logo-img.png) -
  alt text should be **website logo**
- [https://assets.ccbp.in/frontend/react-js/nxt-trendz-login-img.png](https://assets.ccbp.in/frontend/react-js/nxt-trendz-login-img.png) -
  alt text should be **website login**
- [https://assets.ccbp.in/frontend/react-js/nxt-trendz-home-img.png](https://assets.ccbp.in/frontend/react-js/nxt-trendz-home-img.png) -
  alt text should be **clothes that get you noticed**
- [https://assets.ccbp.in/frontend/react-js/nxt-trendz-log-out-img.png](https://assets.ccbp.in/frontend/react-js/nxt-trendz-log-out-img.png) -
  alt text should be **nav logout**
- [https://assets.ccbp.in/frontend/react-js/nxt-trendz-home-icon.png](https://assets.ccbp.in/frontend/react-js/nxt-trendz-home-icon.png) -
  alt text should be **nav home**
- [https://assets.ccbp.in/frontend/react-js/nxt-trendz-products-icon.png](https://assets.ccbp.in/frontend/react-js/nxt-trendz-products-icon.png) -
  alt text should be **nav products**

- [https://assets.ccbp.in/frontend/react-js/nxt-trendz-cart-icon.png](https://assets.ccbp.in/frontend/react-js/nxt-trendz-cart-icon.png) -
  alt text should be **nav cart**

- [https://assets.ccbp.in/frontend/react-js/nxt-trendz-products-img.png](https://assets.ccbp.in/frontend/react-js/nxt-trendz-products-img.png) -
  alt text should be **products**
- [https://assets.ccbp.in/frontend/react-js/nxt-trendz-cart-img.png](https://assets.ccbp.in/frontend/react-js/nxt-trendz-cart-img.png) -
alt text should be **cart**
</details>

<details close>
<summary>Colors</summary>
<br>
<div style="background-color: #1e293b; width: 150px; padding: 10px; color: white">Hex: #1e293b</div>
<div style="background-color: #ffffff; width: 150px; padding: 10px; color: black">Hex: #ffffff</div>
<div style="background-color: #475569; width: 150px; padding: 10px; color: white">Hex: #475569</div>
<div style="background-color: #e6f6ff; width: 150px; padding: 10px; color: black">Hex: #e6f6ff</div>
<div style="background-color: #d7dfe9; width: 150px; padding: 10px; color: black">Hex: #d7dfe9</div>
<div style="background-color: #e2e8f0; width: 150px; padding: 10px; color: black">Hex: #e2e8f0</div>
<div style="background-color: #64748b; width: 150px; padding: 10px; color: black">Hex: #64748b</div>
<div style="background-color: #0b69ff; width: 150px; padding: 10px; color: white">Hex: #0b69ff</div>
<div style="background-color: #ff0b37; width: 150px; padding: 10px; color: white">Hex: #ff0b37</div>
<div style="background-color: #0967d2; width: 150px; padding: 10px; color: white">Hex: #0967d2</div>

</details>

#### Font-families

- Roboto

### ** Concepts used in the application ** </br>
### JWT Token
JSON Web Token is a standard used to create Access Tokens. These access tokens are also called JWT Tokens.</br>

The client uses these access tokens on every subsequent request to communicate with the Server.</br>
While making HTTP Request, we have to send an access token in the HTTP Headers with the key Authorization.</br>
Example:</br>

Authorization: Bearer jwt_token</br>

### Storing JWT Token in State
When we store the JWT Token in the state,</br>

On page refresh, the JWT token won't be available</br>
It is difficult to pass state information to every component</br>


### Storage Mechanisms
### Client-Side Data Storage
Storing Data on the Client
### Server-Side Data Storage
Storing Data on the Server using some kind of Database
--> Different types of Client-Side data storage mechanisms are:</br>

Local Storage</br>
Cookies</br>
Session Storage</br>
IndexedDB, etc.</br>

### Cookies
A cookie is a piece of data that is stored on the user's computer by the web browser.

A cookie is made up of:

Name & Value
Expires − The date the cookie will expire. If this is blank, the cookie will expire when the visitor quits the browser.</br>
Domain − The domain name of your site.</br>
Path − The path to the directory or web page that set the cookie. This may be blank if you want to retrieve the cookie from any directory or page.</br>
Secure − If this field contains the word "secure", then the cookie may only be retrieved with a secure server. If this field is blank, no such restriction exists, etc.</br>

 ### Why Cookies?
With cookies, we can set the expiry duration.

Examples:</br>

Banking Applications - Cookies get expired in minutes</br>
Facebook - Cookies get expired in months or years</br>

### Cookies vs Local Storage
![image](https://user-images.githubusercontent.com/46521639/117770046-14be2480-b252-11eb-8d7e-e05b73ea0b6e.png)

### Third Party Package - js-cookie
JavaScript can read, create, modify, and delete the cookies.</br>

NPM contains a js-cookie, a third-party package to manipulate cookies easily.</br>

Installation Command:   npm install js-cookie --save </br>

js-cookie methods are:

Cookies.set()- It is used to set the cookie</br>
Cookies.get()- It is used to get the cookie</br>
Cookies.remove()- It is used to remove the cookie</br>

### Cookies.set()
** Cookies.set('CookieName', 'CookieValue', { expires: DAYS });

### Cookies.get()
It returns undefined if the cookie does not exist/expire.
** Cookies.get('CookieName');

### Cookies.remove()
** Cookies.remove('CookieName');

### Redirect Component
The react-router-dom provides the Redirect component. It can be used whenever we want to redirect to another path.</br>
Syntax: -  <Redirect to="PATH" />

### Redirect Component vs history Methods
Use the Redirect Component when you have to stop displaying UI and navigate to a route. Ex: Inside Class Component - render()</br>
In all other cases, use history.push() or history.replace() syntax Ex: Ex: onSubmit, onClick event callback functions</br>

**The Redirect component uses the history push and replace methods behinds the scene.

### withRouter
The history prop will be available for only components which are directly given for Route.</br>

To provide history prop to other components, we can wrap it with the withRouter function while exporting it.</br>

Example:</br>
import { withRouter} from 'react-router-dom'
...
export default withRouter(ComponentName)
