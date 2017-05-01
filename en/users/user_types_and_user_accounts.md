---
lang: en
layout: article_with_sidebar
updated_at: '2017-05-01 11:33 +0400'
identifier: ref_PWr4CNvW
title: ''
order: 100
published: true
---
## X-Cart user types
X-Cart has two major types of users depending on the X-Cart store area where they primarily operate:

   *   Administrators (aka admins);
   *   Customers.
   
X-Cart administrators are users with access to the Admin area - the back end of an X-Cart store that provides various tools for the store configuration, as well as the management of products, orders and users. Every X-Cart store has at least one administrator, but may have multiple administrators if the store owner chooses to create additional administrator accounts. Additional administrator accounts may be set up with full or limited access to the stores's back end with the help of _Roles_.

X-Cart customers are users of the Customer area - the zone of an X-Cart store where one can view and buy products. Generally, we may call anyone who views the storefront and acts as a shopper (this includes viewing products, adding products to the shopping cart and placing orders) a "customer". Not all customers, however, are the same: some just browse through the site and leave, others choose to buy stuff. Those who choose to buy stuff may do it as a guest without registering an account, or may prefer to create an account so as to have access to their order history and be able to reuse their registration name and address for future purchases. If we wanted to emphasize the difference between these types of customers, we would say that the ones who come to the store and navigate the site viewing the publicly accessible pages of the Customer area are just "visitors" or "shoppers", the ones who sign up for an account and maintain a user profile with the store are "registered customers", and the ones who make a purchase without creating an account or logging in to an existing account are "anonymous customers". Speaking about the management of X-Cart users, it is only the latter two types of customers that a store administrator may hope to manage. Registered customers have a user account that represents them in the store system and can be used to access their profile information and order history. Anonymous customers do not have an account, but can be traced as a source of orders and can be converted to regular registered customers.

## User management
The management of users in an X-Cart based store takes place in the Users section of the Admin area (**Users** > **Users**). To manage customers, a user must either be an X-Cart administrator with root access or an administrator with the permission to manage users; to manage administrators, a user must be a root administrator or an administrator with the permission to manage administrators (specific permissions can be set via the Roles section of the Admin area (**Users** > **Roles**).

In the Users section of the Admin area, the store users can be seen as a list presented in the form of a table. For each user, the table provides the following information:
     
   *   Login/Email;
   *   Name;
   *   Access level (_Administrator_, _Customer_ or _Anonymous_ + information about the user's membership level; for example, "Customer (VIP customers)" means that the user is a registered customer with the membership level "VIP customers", whereas "Customer (requested for VIP customers)" means that the user is a registered customer and they have submitted a request for "VIP customers" membership which has yet to be approved by the store admin);
   *   Orders (Number of orders placed by the user; the number link can be clicked upon for access to the list of all the orders by this user);
   *   Created (Account creation date);
   *   Last login (Date of the user's latest login to their user account). 
   
The filter above the table can be used to filter the table contents and find specific users.

The administrator with user management permissions can access the profile of any user in the table for viewing/editing. To access the profile of a user, click on the user login/email link in the Login/Email column or the user name link in the Name column. 

The administrator can remove user accounts. To remove a user account, click on the Trash icon opposite the user name in the table column at the far right (this marks the user account for removal), then click **Save changes**.

The administrator can export user account information to CSV format.  To export the entire users table, click the button **Export all: CSV** below the table. To export the information for specific users, mark these users by selecting the check boxes before their names, then click the button **Export selected: CSV** (This button is displayed in the place of the **Export all: CSV** button when at least one user is selected).

The administrator can create new user accounts directly from Users section in the Admin area. To create a new user account, click the **Add user** button above the users table and use the Create profile form to specify the account details for the new user.