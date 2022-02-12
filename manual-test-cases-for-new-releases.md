**If testing on Android, toggle the “Don’t keep activities” option in the developer options.**

### Update

1.  Ensure proper older version is installed:
    
    1.  The device has an installed Plante
        
    2.  The installed Plante is of the previous version.
        
    3.  It has a logged in user.
        
    4.  The “Recent products” screen has at least 1 product.
        
2.  Update to the newer version.
    
3.  Ensure proper newer version:
    
    1.  If the first page now needs to ask more data from the user, it should ask it.
        
    2.  Recent products are shown in the same way as before.
        

### Display product

1.  Scan the barcode of an already stored product.
    
2.  Ensure the proper product’s card is displayed.
    
3.  Ensure product screen is displayed properly.
    

### Add product

1.  Scan the barcode of a product which is not stored both on the Plante backend and the OFF backend.
    
2.  Ensure the product is not found.
    
3.  Input all product packaging data.
    
4.  Put the product onto the map.
    
5.  Save the product.
    
6.  Click on the newly appeared product card on the barcode scanning screen.
    
7.  Ensure the product is properly displayed.
    

### Check the product was added

1.  Scan the recently added product’s barcode.
    
2.  Click on the product card on the barcode scanning screen.
    
3.  Ensure the product is properly displayed.
    
4.  Open the map.
    
5.  Ensure the product is within the shop it was put into.
    
6.  Ensure the product is properly displayed when it is opened from the shop screen.
    

### The “Help with veg-status” button

1.  Open the Products Management page in Web Admin: [https://planteapp.com/plante\_web\_admin/#/manage\_products](https://planteapp.com/plante_web_admin/#/manage_products)
    
2.  Find the just added product by its barcode, erase its vegan status.
    
3.  In the app scan the barcode again and open the product's page.
    
4.  Ensure the product has the “Help with veg-status” button.
    
5.  Help with veg-status, _choose the “I don’t know” option_.
    
6.  In the Products Management page search for product again, ensure it has the “Unknown” status.
    
7.  In the app rescan product’s barcode and ensure it has the “Unknown” option with “Community” as source.
    
8.  Help with veg-status, _choose either the “Positive” or the “Negative” option_.
    
9.  Repeat steps 6 and 7, this time checking for the just selected Positive or Negative status.
    

### Search

1.  Open map, click search bar.
    
2.  Enter a shop name, click “Search”.
    
3.  Ensure the searched shop is found.
    
4.  Click the found shop.
    
5.  Ensure map is opened, scrolled to the shop, shop’s card is opened.
    
6.  Return to search results by clicking on the map search bar.
    
7.  Ensure old search results and query are still displayed.
    
8.  Clear the search query.
    
9.  Enter a road name, click “Search”.
    
10.  Ensure the searched road is found.
    
11.  Click the found road.
    
12.  Ensure map is opened, scrolled to the road.
    

### Fresh install

1.  Copy your tester user’s ID from app’s settings.
    
2.  Open [https://planteapp.com/plante\_web\_admin/#/manage\_users](https://planteapp.com/plante_web_admin/#/manage_users) and delete the user
    
3.  Uninstall the app, install the app again.

4.  Set Username, Self-description, Avatar.

5.  Ensure Username, Self-description and Avatar are properly displayed in the Profile page.
    
6.  Check if map is properly displayed and works.
    
7.  Scan a barcode, ensure the product is properly displayed.
    

### Suggested products

1.  Scroll map to a not-loaded-yet city with:
    
    1.  Country-wide suggestions enabled,
        
    2.  Existing added to the map products by users (confirmed products).
        
2.  Click “Load territory”.
    
3.  Ensure loading of territory and loading of suggestions works well.
    
    1.  Progressbars show some progress,
        
    2.  Hints show proper info.
        
4.  Ensure map has markers for both suggestions and confirmed products.
    
5.  Ensure map filters work properly.
    
6.  Open a shop, ensure it properly displays (the open shops should have all 3 kinds of products):
    
    1.  Confirmed products,
        
    2.  City-wide suggestions,
        
    3.  Country-wide suggestions.
        
7.  Click “Not sold here” on a city-wide and a country-wide suggestion - ensure they’re both gone from the list.
    
8.  Test suggestions confirmation and un-confirmation:
    
    1.  Click “Sold here” on a city-wide and a country-wide suggestion - ensure they’re both added to the confirmed list.
        
    2.  **Then click “Not sold here” on the 2 just added products to not mess up the data of the city.**
        
    3.  Ensure the products are removed from the list.
        
    4.  Restart the app (cold start), ensure the 2 removed products are not confirmed, but are within suggestions.


### Distance units

1.  Move the map to a metric country (if not there yet).

2.  Search for a store.

3.  Ensure distance to found stores is displayed in kilometers and meters.

4.  Move the map to an "Emperial"-country (the US or the UK).

5.  Search for a store.

6.  Ensure distance to found stores is displayed in miles and feet.
