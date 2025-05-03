Custom Cart Drawer – Shopify Dawn Theme
🚀 Project Overview
This project is a custom cart drawer enhancement for Shopify’s Dawn theme. It includes:

- Dynamic product recommendations ("Frequently bought together")

- Social proof (customer reviews directly in the cart drawer)

These features aim to improve the conversion rate and average order value for the store.

🛠️ Setup Instructions
1️⃣ Clone the repository:
git clone https://github.com/YOUR_USERNAME/custom-cart-drawer.git
cd custom-cart-drawer

2️⃣ Set up your Shopify store:
Create a development store via Shopify Partner Dashboard.
Install the Dawn theme.

3️⃣ Push your changes:
Use Shopify's GitHub integration to connect your repo to your theme.
OR manually upload the modified theme files to your store.

4️⃣ Import product data:
Download the product CSV:
Apparel CSV
Go to Products > Import and upload the CSV. (ALREADY DONE IN MY STORE )

✨ Features
🔄 Dynamic Product Upsell
Fetches products from /collections/cart-upsells/products.json

Displays:

Product image (lazy-loaded)

Title, truncated description

Price formatted with currency

Add to Cart button (works via Shopify Cart API without page reload)

⭐ Social Proof Section
Review with:

Avatar image

Star rating

Customer name & testimonial

---- Responsive & Accessible ------
Fully responsive (desktop, tablet, mobile)

Meets WCAG 2.1 AA accessibility:

Semantic HTML

alt text on images

Proper button labels

⚙️ Technical Details
Cart API:
Uses /cart/add.js to add upsell products asynchronously.

Dynamic Loading:
Vanilla JS (fetch()) grabs the product data dynamically from the cart-upsells collection.

Performance:
Lazy-loaded images and scoped JavaScript to avoid conflicts with native Shopify scripts.

Error handling:
Logs fetch/add-to-cart errors in the console.

------ Key Files -------
File	Description
sections/cart-drawer.liquid	Main drawer layout, includes upsell & review sections
assets/cart.js	JavaScript for fetching products & handling add-to-cart
assets/cart-drawer.css	Styling for upsell & review components

------ Challenges & Solutions ---------
Dynamic vs. Liquid:
Shopify Liquid is server-side, so we used JavaScript fetch to dynamically load upsells.

Cart refresh issue:
Originally reloaded the page after adding to cart; optimized it to add without page reload using the Cart API.

------- Improvements to Consider ----------
Make upsells contextual to cart contents.

Add multiple rotating review testimonials.

Show an animated success state when an upsell is added.

🔗 Live Preview
URL: [https://your-store.myshopify.com](https://custom-cart-drawer-test.myshopify.com/)

Password: Password Protected !

 Notes
This project was developed for a technical assessment and uses Shopify’s Dawn theme (MIT license). All upsell features and social proof are designed to be easy to maintain via the Shopify admin panel.
