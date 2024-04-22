Also known as the **Backend**, the **application server** generates content on user-demand which is influenced by certain properties. 

Say you want to look for an email from your personal account.

* You open up the Mail webpage on your browser and login to your account. Up till this point everything is the same for everyone. This is called **Static content**.

* Then appears your inbox and you get the mail you wanted. The inbox that appears is personalized by the **application server** and is called **Dynamic content**.

| Static | Dynamic |
|--|--|
| Does not depend on other attributes | Modified in accordance with certain properties |
| Processed by Web server | Processed by an **Application server** |

## How does it work?

* The **application server** on getting the user input via the **web server** interacts with the database.
* Searches for the data you want.
* Sends it back to you via the **web server**.

![[Pasted image 20230920214753.png]]

#### Efficiency
Application servers are quick-to-respond thanks to the web servers. Web servers use **caching**. 

**Caching** → The content requested by the user gets temporarily stored in the web browser to easily re-deliver it on request.

![[Pasted image 20230920215716.png]]
