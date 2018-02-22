# About this data
This dataset keeps track of inventory since the company started and therefore a large number of items captured in the csv files were sold a long time ago. The business needs a logic that will tell us what’s still in inventory and what’s been sold.

# Metadata 
*Inventory that has the following concatenated locations (BeginInventory Location + ‘-‘ + EndingInventory Location) no longer exists and should be excluded:

 'PURCHASED-PURCHASED',

'STOLEN-STOLEN',

'CUSTOMER_THEFT-CUSTOMER_THEFT',

‘RECEIVING_ERROR_DOES_NOT_EXIST-RECEIVING_ERROR_DOES_NOT_EXIST', 'LOST_AT_WAREHOUSE-LOST_AT_WAREHOUSE',

'DAMAGED-DAMAGED',

'RETIRED-RETIRED',

'MOVED_TO_OUTLET-MOVED_TO_OUTLET',

 'LOST_BY_UPS-LOST_BY_UPS',

'PERMANENTLY_GROUNDED-PERMANENTLY_GROUNDED',

'RETURNED_TO_VENDOR-RETURNED_TO_VENDOR',

'PURCHASED_IMMEDIATE-PURCHASED_IMMEDIATE',

'RECOUPED-RECOUPED',

'MOVED_TO_RENTAL-MOVED_TO_RENTAL',

'PROMOTIONAL_GIVEAWAY-PROMOTIONAL_GIVEAWAY',

'LOST_BY_CUSTOMER-LOST_BY_CUSTOMER'

*Inventory items that we’re bought in the current month would have a previous month’s location of ‘New_Inventory’

*Items that were sold in the current month have the following ending location codes (research what % does if you haven’t used it):

'%-PURCHASED' OR

LIKE 'PURCHASED-%' OR

LIKE 'STOLEN-%' OR

LIKE '%-STOLEN' OR

LIKE '%-RECOUPED' OR

LIKE 'RECOUPED-%'

*For simplicity, the items that were not captured previously can be found in final inventory. Below should give you a hint on how to put together that list.

NOT LIKE '%-DAMAGED' AND

NOT LIKE '%-PURCHASED' AND

NOT LIKE '%-LOST_BY_UPS' AND

NOT LIKE '%-LOST_BY_CUSTOMER' AND

NOT LIKE '%-RECEIVING_ERROR_DOES_NOT_EXIST' AND

NOT LIKE '%-RETURNED_TO_VENDOR' AND

NOT LIKE '%-LOST_AT_WAREHOUSE' AND

NOT LIKE '%-CUSTOMER_THEFT' AND

NOT LIKE '%-RETIRED' AND

NOT LIKE '%-STOLEN' AND

NOT LIKE '%-RECOUPED'

 
