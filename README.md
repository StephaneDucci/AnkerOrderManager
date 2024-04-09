AnkerOrderManager

An Excel file for managing Anker supplies and sales to Coppo customers. Facilitates the registration of customer orders. Creates a dataset with orders allowing for historical data analysis.

V4.0 TO DO

Implementation of automatic emails for managing customer relations.

V3.8

Deleted the "datiPostVendita" dataset. Compensated by adding two columns to "storicoOrdini": COPPO CATEGORY, DATE. With this modification, the "dbOrdini" dataset is complete and it will be possible to extract any information regarding supplies and sub-orders. The post-sales part has been reorganized to be easier to consult. Buttons have been added to navigate between tables and charts. The pages are now clearer. All pivot tables now refer to the "dbOrdini" dataset.

V3.7

Added the possibility to select the data loading mode:
A = Data taken from the current list
B = Data taken from the order history
Removed the "listaCecila" and "listaCategorie" sheets, replaced by "listeSpeciali". The sheet has been organized, making it easier for a third-party user to intervene on these lists.

V3.6 DONE

Added the ability to modify and save an order even in "COMPLETED" mode. Added post-order management. Management of ordered bottle availability.

V3.5 DONE

In the ORDER FORM, replaced the TOTAL column with:
TOTAL ANKER COST
TOTAL IMPORT COST
TOTAL SELLING PRICE
Eliminated other minor bugs:
Incorrect rounding in price calculation in pro forma and ORDER FORM. Now follows the calculation method used in the LISTONE sheet. Before saving, remove filters and hidden rows in ORDER FORM. Automatic pro forma still in testing phase but still some small details corrected. Added 3 sheets for data analysis:
SUPPLY ANALYSIS
Useful for having some insights into the supply as a whole. Should give an EXACT estimate of the total Anker pro forma.
ORDERS ANALYSIS
To see at a glance the order situation.
PRODUCTS ANALYSIS
To see if useful. The idea is to understand which products are most requested and which category they belong to.
DAA CALCULATOR (just an idea)
To automatically create the DAA in and out? IN TEST Added sheet locking for ORDER FORM to prevent a user from modifying and breaking it. All cells needed for data entry by the user have been unlocked. TO VERIFY THAT ALL MACROS AND VBA CODE DO NOT CONFLICT WITH THE LOCK. IN THAT CASE, EITHER UNLOCK THE CELLS THAT INTERACT WITH THE VBA CODE OR ADD IN THE VBA CODE THE UNLOCKING OF THE SHEET AND RELOCKING IT.

V3.4

Eliminated customer tabs. Eliminated the store module. Now all orders are managed by the customer module, which will be renamed "ORDER FORM" from which it will be possible to save, load, and modify orders both for customers and stores. Created a "dbOrders", a large dataset where all orders are recorded. Each record in the dataset represents a reference ordered by one of our customers or Coppo stores. Each record has specific fields for identification and association with the correct customer and correct supply. Each supply has been assigned a distinctive code of the type MMMYY. The dataset thus formed will be useful for analysis on: PRODUCTS, CUSTOMERS, CROSS PRICES FOREIGN AND NATIONAL SUPPLIERS added a "find vinolux sku" block to facilitate matching the vinolux sku and therefore the competitor's price Added a series of small features to make the user experience smoother: select distinct customers based on the selected supply buttons: RESET FORMULAS, CUSTOMERS, SHOW HISTORY Implemented pro forma generation (still in test) Created a button to generate a backup of dbOrders

V3.3 BUG FIXES

Added filter for products not available in power query. Corrected the "customer module" and the "store module" to take into account purchase prices rather than selling prices. Corrected the "customer module" and the "store module" so that orders are entered with the count of bottles rather than cartons.

Fully Achieved Objectives by 3.2

Quick creation of the necessary price lists to request orders from customers and our stores. Recording orders received from customers

Objectives Yet to Be Achieved

Extended testing of the application Addition of a system for managing availability and adapting orders to these Creating a relationship between Anker sku and Geko sku Automatic email sending Completion of the blacklist (Cecilia's list) with as many references as possible to be eliminated Understanding whether mixed spirits should be included in the price list to be proposed to wine shops/wholesalers (they should definitely be proposed to stores) In the customer module, add a column with the cost price. So that when calculating the aggregated order, you already know how much you will spend.

Update 3.2

Fixed Bugs

Eliminate every duplicate present in the list! Duplicates make vertical search by reference name ineffective! Handle the bug that leads to not correctly selecting the range to copy when importing a customer order on a new supply.

Features Deployed

Create a new button in the control panel "New Store Order". Being the store order larger and not requiring a pro forma, it must have a different layout. Eliminate the merging of category title cells in the warehouse list.

Other

Cleanup among named ranges (will need to verify if others will be recreated) small optimizations in scripts

STILL TO BE FIXED AND IMPROVED:

Sheet with physical addresses of customers. Those who place the order (Davide and Lorenzo) should be able to see the stock quantities of the product in question (DIFFICULT TO IMPLEMENT WOULD REQUIRE A DATASET WITH THE CROSS REFERENCES BETWEEN COPPO SKUs AND ANKER SKUs).
