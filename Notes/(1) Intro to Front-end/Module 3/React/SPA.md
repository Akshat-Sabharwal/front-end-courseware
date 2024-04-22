**Single Page Application** or an **SPA** is a webpage that uses **Dynamic content** and updates when needed rather than being replaced by other webpages.

A traditional website is basically *a web of pages with static elements linked to each other*. 


![[Pasted image 20230920220817.png|400]]


It would be inefficient for the web browser to render and reload different pages for every request. Thus **SPAs** are used.

## How they work
There are two types of working of SPAs
#### Bundling
The web server on the initial request for a webpage unloads and sends back all the required HTML, CSS and JavaScript documents.



![[Pasted image 20230920221716.png|500]]


#### Lazy Loading
On every subsequent request, the web server delivers data packets in the **JSON** format which are rendered in the same webpage and updated.



![[Pasted image 20230920221118.png|500]]


