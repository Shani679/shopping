# Online supermarket - online shopping
Online supermarket is a web application of a self-service virtual supermarket that includes various grocery and food products arranged by categories, allowing the user (customer) to fill up a virtual shopping cart and make an order. <br />
There is also an admin user who is allowed to add new products and new categories to the supremarket, edit their details (name, price, image) or remove them.
## Built with
Client | Server | Database <br/>
------ | ------ | --------
Html5 | Node.js | Mongo DB
CSS3 | Express.js |
Bootstrap 3.3.7|
Angular.js
## How it works
* Each user who is signed in can browse the virtual store, fill up a virtual cart with products, make an order and choose a date for a direct delivery to his home.
* New users can sign up by email or sign in by their Facebook or Google account.
* Once the user is signed in, he will be associated with a **SESSION** in the server and a button of "Start shopping" will be displayed. In case of a returning user, a message about an active cart will be displayed to the user or message about his last order (if he doesn't have an active cart). By clicking on the button the user will be taken to the shopping page. 
* Once the user has been redirected to the shopping page he will be able to fill up the cart or see his active cart with the products that he already added, and continue the shopping from the point where he stopped.
* What can the user do in the shopping page?
  * Search for products by category or by typing the product's name.
  * Add products to cart by selecting quantity and clicking on "ADD TO CART" button.
  * Remove a product from the cart.
  * Empty the whole cart. <br/><br/>
* **In each interaction with the shopping cart, the user will see the updated price at the bottom of the cart.**
* At any point, the user can leave the website, return at another time and continue the shopping exactly from that point (unless the user logged out).
* By clicking on the CHECKOUT button, the user will be required to fill out the shipping details:
  * Shipping address
  * Payment details
  * Shipping date
* No shipping will be made for a given day, for which three orders have already been made (by other users).
* After placing the order, the shopping cart (stored on the session) will be stored in the database under the orders collection and will be assigned to the logged-in user.
* Also, at this point the user will have an option to download a receipt.
* As noted above, the next time the user will log in to the website, a message with details about his last order will be displayed to him.
* An admin user who is logged in will be taken to the products management page where he will be able to add, edit or delete products offered for purchase.
