# Products management full-stack web application for the Bluevelvet Music Store
A products management full-stack web application made using HTML, CSS,JavaScript for the frontend and Spring Boot for the backend.  The user can register and login. 

This application is used in the course Web Programming, taught by Rodrigo Martins Pagliares and Fellipe Guilherme Rey de Souza at the undergraduate Computer Science course at UNIFAL-MG - Brazil.

You can try the the webapplication without configuring the backend and a MySQL database. The front-end is self-contained and can be used to perform simple CRUD operations on products table upon logging in. The data is stored and retrieved from LocalStorage.

## Technologies Used (frontend)

- HTML
- CSS
- JavaScript
- Font Awesome
- Box Icons
- Google Fonts

## Technologies Used (backend)

- Spring Boot (including Spring Security)
- MySQL

## Requirements

### US-1050: Add product

"As an Administrator I want to add a product to increase the the variaty of music product sold by BlueVelvet Music Store"

Acceptance criteria:

- Only authenticated users in the role orf admin or editor can manage products.
- A product has a name, short description, full description, brand, category, main image, featured images, list price, discount percent, enabled, in stock, creation time and update time, length, witdh, height, weight, cost, product details
- Name: Name of the product (must be unique)
- Short description: Short description
- Full description: Detailed description
- Brand: Brand of the product
- Category: Category to which the product belongs
- Main image: Primary product image - used in listing pages
- Featured images: Other images describing the product
- List price: Sell price
- Discount: Discount applied to the Sell price
- Enabled: Whether the product is displayed or not for shopping
- In Stock: Whether the product is available or not in stock
- Creation time: Time the product was first created
- Update time: Time the product was last updated
- Length, witdh, height, weight: Dimensions (used for shipping cost calculation). Units used: inch and pound. The dimensions is for the box that is used to package the product - not the product's dimension.
- Cost: Used for revenue report
- Produt details: Name/value pairs with details for the product. 
      - e.g Track 1 - Karma Police
               Track2 - Airbag
- Note:
1. Make Products Page Fully Responsive
2. Reuse a rich text editor component to ease including the short and full descriptions or use a simple textarea components?
https://www.jqueryscript.net/text/Rich-Text-Editor-jQuery-RichText.html
- Automate the creation of some sample products to ease testing (SQL script, programmatically?), including some sample product images
- Test: Create 3 products
- TODO: Implement I18N? Use cm, m, g, and kg?
- It must be implemented a mechanism to uploa the main and featured images. It must be accepted png images.
- Possible directory structure for product images:
    product-images/
          ----- 1/
                                        ........... main-image.png
           ----- extra-images/
                                      ........ extra-image-1.png
                                      ......... extra-image-2.png 
           ----- 2/
                                        ........... main-image.png
           ----- extra-images/
                                      ........ extra-image-1.png

### US-1452: Edit product information

"As an Administrator I want to edit the data of an exiting product to improve/fix the information of the products sold by Blue Velvet Music Store."

Acceptance criteria:

- Only authenticated users in the role orf admin or editor can edit the data of products. A user playing the role of salesperson can update the price of a procuct, but not other product details.
- All fields of a product may be updated.  
- See US-1645 for the product fields.
- Test Get a product
- Test Updating Extra Images:
   - Change an existing extra image
   - Remove an existing one
   - Add a new product detail
- Test Updating Details:
- Change an existing product detail 
- Remove an existing product detail
- Test Updating Price -  Remaining information should remain unchanged.
- Test Updating Overview, Main image, Description & Shipping
- A form is displayed with the products data already filled in.
- Note: Make Products Page Fully Responsive


### US-2032: List products for administrators

"As an Administrator I want to list all of products in order to have a global view of all products  sold on Blue Velvet Music store."

Acceptance criteria:

- Only authenticated users in the role orf admin, salesperson or shipper can list products.
- The list of products may be too long. Provide a way for navigation (e.g. pagination for the products list)
 - By default, it must be possible to see 10 products per page (pagination)
- Pagination is based on product names 
- Pagination should work well with sorting 
- Sort by product name, ID, brand, and category
- Default sorting by name, ascending order
- Filter: search by product name, short description, full description, brand name, and category name
- The fields main image, product name, brand, and category must be shown
- To see product details, see US-1045
- Note: Make Products Page Fully Responsive.

### US-1045: View product details for administrators

"As an Administrator I want to view product details in order verify if all relevant product information is available."

- Different of US-2032 where it is possible to see some product fields, this US allows the Administrator to visualize all product details (fields) for a specific product.
- The product details must be shown in the same screens created in the US-1645 - Create Product

 ### US-1627: Delete product

 "As an Administrator I want to delete a product in order to have only products that are sold by Blue Velvet Music Store."

 - Only authenticated users in the role orf admin or editor can delete products.
- Also delete the product images in procucts-image directory
- Test Delete a product
- A message must be displayed asking you whether you want to delete this product or not.
- Note: Make Products Page Fully Responsive

 ### Other requirements
- Registration
  - Users can register a new account
- Login
  - Users can login using their registered accounts
- Logout
  - A user can logout once logged in.
- Error Page
  - if a user tries to access the dashboard page without logging in then an error page is displayed.
- Sorting by columns
  - Each column is sortable. Click the column name to see the feature at play.
- Filtering by columns
  - You can select the column you want to and search specific entries.


 

